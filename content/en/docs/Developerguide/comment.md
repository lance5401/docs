# COMMENT<a name="EN-US_TOPIC_0242370557"></a>

## Function<a name="en-us_topic_0237122093_en-us_topic_0059778518_se3f65a35f2604b18a7024290d26f80cf"></a>

**COMMENT**  defines or changes the comment of an object.

## Precautions<a name="en-us_topic_0237122093_en-us_topic_0059778518_s1a808d6187aa43c5bda33df14effd78f"></a>

-   Each object stores only one comment. Therefore, you need to modify a comment and issue a new  **COMMENT**  command to the same object. To delete the comment, write  **NULL**  at the position of the text string. When an object is deleted, the comment is automatically deleted.
-   Currently, there is no security protection for viewing comments. Any user connected to a database can view all the comments for objects in the database. For shared objects such as databases, roles, and tablespaces, comments are stored globally so any user connected to any database in the cluster can see all the comments for shared objects. Therefore, do not put security-critical information in comments.
-   For most objects, only the owner of the object can set comments. Roles do not have owners, so the rule for  **COMMENT ON ROLE**  is that you must be an administrator to comment on an administrator role, or have the  **CREATEROLE**  permission to comment on non-administrator roles. A system administrator can comment on all objects.

## Syntax<a name="en-us_topic_0237122093_en-us_topic_0059778518_sc17f26ffc35449b285334777c0405013"></a>

```
COMMENT ON
{
  AGGREGATE agg_name (agg_type [, ...] ) |
  CAST (source_type AS target_type) |
  COLLATION object_name |
  COLUMN { table_name.column_name | view_name.column_name } |
  CONSTRAINT constraint_name ON table_name |
  CONVERSION object_name |
  DATABASE object_name |
  DOMAIN object_name |
  EXTENSION object_name |
  FOREIGN DATA WRAPPER object_name |
  FOREIGN TABLE object_name |
  FUNCTION function_name ( [ {[ argmode ] [ argname ] argtype} [, ...] ] ) |
  INDEX object_name |
  LARGE OBJECT large_object_oid |
  OPERATOR operator_name (left_type, right_type) |
  OPERATOR CLASS object_name USING index_method |
  OPERATOR FAMILY object_name USING index_method |
  [ PROCEDURAL ] LANGUAGE object_name |
  ROLE object_name |
  SCHEMA object_name |
  SERVER object_name |
  TABLE object_name |
  TABLESPACE object_name |
  TEXT SEARCH CONFIGURATION object_name |
  TEXT SEARCH DICTIONARY object_name |
  TEXT SEARCH PARSER object_name |
  TEXT SEARCH TEMPLATE object_name |
  TYPE object_name |
  VIEW object_name
}
   IS 'text';
```

## Parameter Description<a name="en-us_topic_0237122093_en-us_topic_0059778518_s56dde1ab6b0149328413f05ffc3c73b8"></a>

-   **agg\_name**

    Specifies the new name of an aggregation function.

-   **agg\_type**

    Specifies the data type of the aggregation function parameters.

-   **source\_type**

    Specifies the source data type of the cast.

-   **target\_type**

    Specifies the target data type of the cast.

-   **object\_name**

    Specifies the name of an object.

-   **table\_name.column\_name**

    **view\_name.column\_name**

    Specifies the column whose comment is defined or modified. You can add the table name or view name as the prefix.

-   **constraint\_name**

    Specifies the table constraint whose comment is defined or modified.

-   **table\_name**

    Specifies the name of a table.

-   **function\_name**

    Specifies the function whose comment is defined or modified.

-   **argmode,argname,argtype**

    Specifies the schema, name, and type of the function parameters.

-   **large\_object\_oid**

    Specifies the OID of the large object whose comment is defined or modified.

-   **operator\_name**

    Specifies the name of the operator.

-   **left\_type,right\_type**

    Specifies the data type of the operator parameters \(optionally schema-qualified\). If the prefix or suffix operator does not exist, the  **NONE**  option can be added.

-   **text**

    Specifies the comment content.


## Examples<a name="en-us_topic_0237122093_en-us_topic_0059778518_s57de72dc01404015a1a8a938238ad917"></a>

```
postgres=# CREATE TABLE tpcds.customer_demographics_t2
(
    CD_DEMO_SK                INTEGER               NOT NULL,
    CD_GENDER                 CHAR(1)                       ,
    CD_MARITAL_STATUS         CHAR(1)                       ,
    CD_EDUCATION_STATUS       CHAR(20)                      ,
    CD_PURCHASE_ESTIMATE      INTEGER                       ,
    CD_CREDIT_RATING          CHAR(10)                      ,
    CD_DEP_COUNT              INTEGER                       ,
    CD_DEP_EMPLOYED_COUNT     INTEGER                       ,
    CD_DEP_COLLEGE_COUNT      INTEGER
)
WITH (ORIENTATION = COLUMN,COMPRESSION=MIDDLE)
;

-- Comment out the tpcds.customer_demographics_t2.cd_demo_sk column.
postgres=# COMMENT ON COLUMN tpcds.customer_demographics_t2.cd_demo_sk IS 'Primary key of customer demographics table.';

-- Create a view consisting of rows with c_customer_sk less than 150.
postgres=# CREATE VIEW tpcds.customer_details_view_v2 AS
    SELECT *
    FROM tpcds.customer
    WHERE c_customer_sk < 150;

-- Comment out the tpcds.customer_details_view_v2 view.
postgres=# COMMENT ON VIEW tpcds.customer_details_view_v2 IS 'View of customer detail';

-- Delete the view.
postgres=# DROP VIEW tpcds.customer_details_view_v2;

-- Delete the tpcds.customer_demographics_t2 table.
postgres=# DROP TABLE tpcds.customer_demographics_t2;
```


备份
```language
Create table staff_copy (Select * from staff);

```
条件更新
```language
UPDATE staff x
INNER JOIN (
	SELECT
		*
	FROM
		staff x
	WHERE
		x.`NAME` LIKE 'LY%'
) y ON x.STF_ID = y.STF_ID
SET x.`NAME` = CONCAT(y. NAME, '=')
```
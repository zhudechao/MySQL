```
group_concat 一对多搜索，字段拼接。


SELECT u.*, ( SELECT group_concat(ar.role_name) FROM auth_role ar WHERE find_in_set(ar.id, u.role) ) AS  cc FROM users u;
```


insert into  select 语法

INSERT INTO imei_record ( user_id, imei, zuk_user, status, create_time ) SELECT id,imei,zuk_user,1,now() from acct_user WHERE id=255642


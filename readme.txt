echo "# docker-spring-boot" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/givet/docker-spring-boot.git
git push -u origin master


docker container run -p 3000:7001  --rm wubhimg/spring-boot-demo 
docker exec -it 22e01685c637 sh
docker inspect 234123414
���� Mounts�µ�ÿ����Ϣ��¼��������һ�����ص����Ϣ��"Destination" ֵ�������Ĺ��ص㣬"Source"ֵ�Ƕ�Ӧ������Ŀ¼��

���Կ������ַ�ʽ��Ӧ������Ŀ¼���Զ������ģ���Ŀ�Ĳ��������������޸ģ������ö����������

 find /var/lib/docker -name happiness.wbh	

 create table t_user( user_id int not null auto_increment,  user_name varchar(30), primary key(user_id) );

insert into t_user(user_name) values('test123');

mysqladmin -u root -p variables | grep datadir


mysql> show variables like 'innodb_%';

/etc/mysql/my.cnf

docker container run   -d   --rm   --name wordpressdb   --env MYSQL_ROOT_PASSWORD=123456   --env MYSQL_DATABASE=wordpress   mysql:5.7


docker run --rm --name mastermysql -d -p 3307:3306 -e MYSQL_ROOT_PASSWORD=123456 --env MYSQL_DATABASE=testdb -v /home/wubh/docker-mysql/master/data:/var/lib/mysql -v /home/wubh/docker-mysql/master/conf/my.cnf:/etc/mysql/my.cnf  mysql:5.7

docker run --rm --name slavemysql -d -p 3308:3306 -e MYSQL_ROOT_PASSWORD=123456 --env MYSQL_DATABASE=testdb -v /home/wubh/docker-mysql/slave/data:/var/lib/mysql -v /home/wubh/docker-mysql/slave/conf/my.cnf:/etc/mysql/my.cnf  mysql:5.7

change master to master_host='172.17.0.3',master_user='backup',master_password='123456',master_log_file='mysql-bin.000004',master_log_pos=1954,master_port=3306;
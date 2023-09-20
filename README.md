ссылка на файл Docker:
docker run --hostname=b88273fa64c3 --mac-address=02:42:ac:11:00:02 --env=PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin --env=GOSU_VERSION=1.16 --env=LANG=en_US.utf8 --env=PG_MAJOR=16 --env=PG_VERSION=16.0-1.pgdg120+1 --env=PGDATA=/var/lib/postgresql/data --env=POSTGRES_PASSWORD=secret --env=POSTGRES_USER=username --env=POSTGRES_DB=database --volume=/var/lib/postgresql/data -p 5432:5432 --restart=no --runtime=runc -d test_image:latest

команды по сбору образа и запуску контейнера 
-docker build -t test_image:latest
-docker run --rm --name test_container –p 5439:5432 -d test_image:latest
-cd C:\Users\Yana\Desktop\Work\docker\db
-docker exec -it test_container psql -U username -d database
-CREATE TABLE IF NOT EXISTS public.index_mass (  user_id BIGINT,  weight BIGINT,  
  height BIGINT);
-INSERT INTO public.index_mass (user_id, weight, height) VALUES  (4, 151, 152),  (5, 153, 
  154),  (6, 155, 156);
-docker exec -it test_container psql -U postgres
-docker run --rm -d --name test_container -p 5432:5432 -v /data:/var/lib/postgresql/data 
  test_image:latest
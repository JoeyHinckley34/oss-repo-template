# Database Lab

## Step 1
http://localhost:5984/ <br />
<img width="1436" alt="Screen Shot 2022-04-04 at 9 58 08 PM" src="https://user-images.githubusercontent.com/50917542/161664171-dc62271d-f888-468c-9f7e-9213b9028831.png"> <br />

## Step 2
curl http://127.0.0.1:5984/ <br />
<img width="891" alt="Screen Shot 2022-04-04 at 10 02 28 PM" src="https://user-images.githubusercontent.com/50917542/161664561-d8df281a-ff4f-4d93-bac1-86ba7a75b6a2.png"> <br />

 curl -X GET http://admin:stickynotes2022@127.0.0.1:5984/_all_dbs <br />
 <img width="689" alt="Screen Shot 2022-04-04 at 10 18 19 PM" src="https://user-images.githubusercontent.com/50917542/161666166-e242732d-285a-44c5-9c33-3195c990b21f.png"> <br />
 
 curl -X PUT http://admin:password@127.0.0.1:5984/baseball  <br />
<img width="704" alt="Screen Shot 2022-04-04 at 10 19 21 PM" src="https://user-images.githubusercontent.com/50917542/161666253-49442eb6-3829-4675-9369-3b7bed4c0639.png"> <br />


curl -X PUT http://admin:stickynotes2022@127.0.0.1:5984//plankton  <br />
curl -X GET http://admin:stickynotes2022@127.0.0.1:5984/_all_dbs   <br />
<img width="685" alt="Screen Shot 2022-04-04 at 10 24 30 PM" src="https://user-images.githubusercontent.com/50917542/161666751-6405cd32-bebd-40e6-a93c-a06723b40dd0.png">


curl -X DELETE http://admin:stickynotes2022@127.0.0.1:5984//plankton <br />
curl -X GET http://admin:stickynotes2022@127.0.0.1:5984/_all_dbs   <br />
<img width="723" alt="Screen Shot 2022-04-04 at 10 22 19 PM" src="https://user-images.githubusercontent.com/50917542/161666528-b32b75f1-fe67-42c4-bc1c-d47125e1d174.png"> <br />

http://127.0.0.1:5984/_utils/ <br />
<img width="1440" alt="Screen Shot 2022-04-04 at 10 25 29 PM" src="https://user-images.githubusercontent.com/50917542/161666835-7838feb4-59de-48e5-acf6-452b2318c051.png"> <br />

hello_world db <br />
<img width="1144" alt="Screen Shot 2022-04-04 at 10 27 27 PM" src="https://user-images.githubusercontent.com/50917542/161667024-6148ddbb-36b3-4589-ab1b-7ee5b8a66c74.png"> <br />

mango query json view <br />
<img width="1361" alt="Screen Shot 2022-04-04 at 10 37 27 PM" src="https://user-images.githubusercontent.com/50917542/161668082-693657f8-c4f2-45a5-aa27-544105f61363.png"> <br />

new query in table view  <br />
<img width="1357" alt="Screen Shot 2022-04-04 at 10 38 46 PM" src="https://user-images.githubusercontent.com/50917542/161668210-90728b8a-3e6e-412d-bc4b-41fbc3608072.png"> <br />
replication complete <br />
<img width="1370" alt="Screen Shot 2022-04-04 at 10 40 47 PM" src="https://user-images.githubusercontent.com/50917542/161668390-8e68dea3-fc8e-44ed-8740-c8b834b70aa5.png"> <br />
hello-world and hello-replication have the same number of docs <br />
<img width="1223" alt="Screen Shot 2022-04-04 at 10 41 23 PM" src="https://user-images.githubusercontent.com/50917542/161668451-bbd3965f-c74f-4a06-83a8-a5590dabea36.png"> <br />

## Step 3
curl http://127.0.0.1:5984/ <br />
curl -X PUT http://admin:stickynotes2022@127.0.0.1:5984/albums <br />   
curl -X PUT http://admin:stickynotes2022@127.0.0.1:5984/albums <br />
<img width="910" alt="Screen Shot 2022-04-04 at 11 02 20 PM" src="https://user-images.githubusercontent.com/50917542/161670602-e923e162-7e73-4c54-9fc3-6ea1c62f46b0.png"> <br />

curl -vX PUT http://admin:stickynotes2022@127.0.0.1:5984/albums-backup <br />
<img width="898" alt="Screen Shot 2022-04-04 at 11 08 51 PM" src="https://user-images.githubusercontent.com/50917542/161671232-e2f89a07-21ba-4051-890b-fe9e38d91053.png"> <br />

curl -vX DELETE http://admin:stickynotes2022@127.0.0.1:5984/albums-backup <br />
<img width="747" alt="Screen Shot 2022-04-04 at 11 09 54 PM" src="https://user-images.githubusercontent.com/50917542/161671332-96aa0e38-e716-4d24-a921-b5259126c7a1.png"> <br />

curl -X PUT http://admin:password@127.0.0.1:5984/albums/6e1295ed6c29495e54cc05947f18c8af -d '{"title":"There is Nothing Left to Lose","artist":"Foo Fighters"}' <br />
curl -X GET http://admin:stickynotes2022@127.0.0.1:5984/albums/6e1295ed6c29495e54cc05947f18c8af  <br />
<img width="902" alt="Screen Shot 2022-04-04 at 11 23 33 PM" src="https://user-images.githubusercontent.com/50917542/161672652-1a80ea84-5b61-449b-8c7e-780849df9160.png">  <br />

curl -X PUT http://admin:stickynotes2022@127.0.0.1:5984/albums/6e1295ed6c29495e54cc05947f18c8af \
     -d '{"title":"There is Nothing Left to Lose","artist":"Foo Fighters","year":"1997"}' <br />
<img width="938" alt="Screen Shot 2022-04-04 at 11 33 37 PM" src="https://user-images.githubusercontent.com/50917542/161673571-129e6c63-d389-483f-a629-4a565fe3da0e.png"> <br />

curl -vX PUT http://admin:stickynotes2022@127.0.0.1:5984/albums/70b50bfa0a4b3aed1f8aff9e92dc16a0 \
     -d '{"title":"Blackened Sky","artist":"Biffy Clyro","year":2002}' <br />
<img width="922" alt="Screen Shot 2022-04-04 at 11 37 24 PM" src="https://user-images.githubusercontent.com/50917542/161674039-c32d21b6-848d-4ad4-a7bd-6d4493e7d7b0.png"> <br />

curl http://admin:password@127.0.0.1:5984/albums/6e1295ed6c29495e54cc05947f18c8af <br />
<img width="1075" alt="Screen Shot 2022-04-04 at 11 39 36 PM" src="https://user-images.githubusercontent.com/50917542/161674220-4501271c-8c43-45af-8bd9-2fbd5104f5d9.png"> <br />

curl -X PUT http://admin:stickynotes2022@127.0.0.1:5984/albums-replica  <br />
curl -vX POST http://admin:stickynotes2022@127.0.0.1:5984/_replicate \ <br />
     -d '{"source":"http://127.0.0.1:5984/albums","target":"http://127.0.0.1:5984/albums-replica"}' \ <br />
     -H "Content-Type: application/json" <br />
<img width="717" alt="Screen Shot 2022-04-04 at 11 41 19 PM" src="https://user-images.githubusercontent.com/50917542/161674427-3beee0b4-5fa7-4c00-8640-dc68e9e74178.png"> <br />

## Step 4
1 <br />
<img width="1112" alt="Screen Shot 2022-04-04 at 11 46 10 PM" src="https://user-images.githubusercontent.com/50917542/161674858-8bd482eb-b67e-4b96-a047-287a66ac04f0.png"> <br />
2 <br />
<img width="1109" alt="Screen Shot 2022-04-04 at 11 48 24 PM" src="https://user-images.githubusercontent.com/50917542/161675156-047b9e10-86ba-474b-8f2f-6299b107678c.png"> <br />
3 <br />
<img width="822" alt="Screen Shot 2022-04-04 at 11 50 19 PM" src="https://user-images.githubusercontent.com/50917542/161675307-7c99b644-ca46-4d26-bcda-f4b68ea281cb.png">
4 <br />
<img width="1113" alt="Screen Shot 2022-04-04 at 11 51 14 PM" src="https://user-images.githubusercontent.com/50917542/161675405-c7fd6119-46db-4f22-8dbb-e3b4f9f3c4d2.png"> <br />





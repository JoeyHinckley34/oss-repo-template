# Database Lab

### Step 1
http://localhost:5984/ <br />
<img width="1436" alt="Screen Shot 2022-04-04 at 9 58 08 PM" src="https://user-images.githubusercontent.com/50917542/161664171-dc62271d-f888-468c-9f7e-9213b9028831.png"> <br />

### Step 2
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




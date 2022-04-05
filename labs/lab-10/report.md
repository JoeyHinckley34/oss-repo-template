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
<img width="673" alt="Screen Shot 2022-04-04 at 10 20 18 PM" src="https://user-images.githubuser![Uploading Screen Shot 2022-04-04 at 10.21.56 PM.png…]()
content.com/50917542/161666352-e840cbb7-9b3f-43a1-a5a7-e71cd80a56a7.png">   <br />

curl -X DELETE http://admin:stickynotes2022@127.0.0.1:5984//plankton <br />
curl -X GET http://admin:stickynotes2022@127.0.0.1:5984/_all_dbs   <br />
<img width="723" alt="Screen Shot 2022-04-04 at 10 22 19 PM" src="https://user-images.githubusercontent.com/50917542/161666528-b32b75f1-fe67-42c4-bc1c-d47125e1d174.png"> <br />

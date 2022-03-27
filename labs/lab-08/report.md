# Lab 8

### Part 1 
Cmake clone <br />
<img width="830" alt="Screen Shot 2022-03-26 at 4 37 34 PM" src="https://user-images.githubusercontent.com/50917542/160256240-d675f822-8f0f-46e9-abf5-1f42d3091597.png"> <br />
Cmake-gui Original Configuration  <br />
<img width="658" alt="Screen Shot 2022-03-26 at 4 57 59 PM" src="https://user-images.githubusercontent.com/50917542/160256824-2f9877ec-cea1-4f9a-9741-f5edc394a7ab.png">  <br />
Cmake-gui Configuration and Generation  <br />
<img width="655" alt="Screen Shot 2022-03-26 at 4 59 52 PM" src="https://user-images.githubusercontent.com/50917542/160256898-b63ebe38-a8f1-41ed-be7e-96378d17df33.png">  <br />
Successful build <br />
<img width="676" alt="Screen Shot 2022-03-26 at 5 12 39 PM" src="https://user-images.githubusercontent.com/50917542/160257307-9c00688c-afed-4d08-9bdb-344ecce30224.png">  <br />


### Part 2
Nghtly Test<br /> 
<img width="1409" alt="Screen Shot 2022-03-26 at 7 35 04 PM" src="https://user-images.githubusercontent.com/50917542/160260528-33e97d91-e8d2-4cc5-bb9c-246b35aff021.png"> <br />
Nightly usage graph <br />
<img width="881" alt="Screen Shot 2022-03-26 at 7 33 39 PM" src="https://user-images.githubusercontent.com/50917542/160260509-1e022158-88d9-4e65-b05f-b99175073ba5.png"> <br />
Expiremental Test<br />
<img width="1411" alt="Screen Shot 2022-03-26 at 7 34 29 PM" src="https://user-images.githubusercontent.com/50917542/160260518-85d95d9f-c822-4f3d-972d-82ae90e3ec4b.png"> <br />
A Test with a Fail ! <br />
<img width="1422" alt="Screen Shot 2022-03-26 at 7 37 56 PM" src="https://user-images.githubusercontent.com/50917542/160260596-b3f73e7a-4e89-498c-8e99-bb23f7d0c9a1.png"> <br />
The error condition was unstable <br />
<img width="1250" alt="Screen Shot 2022-03-26 at 7 40 50 PM" src="https://user-images.githubusercontent.com/50917542/160260639-3d7d971e-0026-4310-aeab-f3261c6f2cd5.png"> <br />
This tells you exactly whats being tested and what failed.  <br />
<img width="1043" alt="Screen Shot 2022-03-26 at 7 41 29 PM" src="https://user-images.githubusercontent.com/50917542/160260659-4f4edbf2-48f3-4786-91a9-394a4b47953b.png"> <br />
This is the change that caused the error.  <br />
This is cmake for xcode which is showing no errors or any failed tests at the moment <br />
<img width="415" alt="Screen Shot 2022-03-26 at 7 42 41 PM" src="https://user-images.githubusercontent.com/50917542/160260685-eecc89c8-417c-477f-8e2d-6a0c358b2d85.png">
Output of: <br />
ctest -D Experimental -I 11,30 <br />
<img width="524" alt="Screen Shot 2022-03-26 at 8 00 59 PM" src="https://user-images.githubusercontent.com/50917542/160261001-f24fee5b-67f5-4a46-9352-66f84a2eef71.png"> <br />
<img width="805" alt="Screen Shot 2022-03-26 at 8 01 10 PM" src="https://user-images.githubusercontent.com/50917542/160261007-b7cee05a-74cf-4a77-bd29-f8f3e47a590a.png"> <br />



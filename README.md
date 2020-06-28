# Task-2
This task is about again integrating jenkins,git,docker with some new concepts like sending mail and automatic lauching a new container if container fails.
For building this steps that we have to follow:

**1. Create container image that’s has Jenkins installed  using dockerfile.**<br><br>
Dockerfile:
![1](https://user-images.githubusercontent.com/48363834/85943091-5fd98c80-b94b-11ea-84a6-85cf41a3e7e3.PNG)

For building image:
>#docker build -t <image_name> <path_of_dockerfile><br><br>
 
![a](https://user-images.githubusercontent.com/48363834/85943092-61a35000-b94b-11ea-8043-6fc862e1ee61.PNG)
![b](https://user-images.githubusercontent.com/48363834/85943097-649e4080-b94b-11ea-97e0-7914c86f74cb.PNG)

Launch a container through this image.<br><br>
![c](https://user-images.githubusercontent.com/48363834/85943219-3cfba800-b94c-11ea-9f0a-b3ec112489f7.PNG)


**2. When we launch this image, it should automatically starts Jenkins service in the container.**<br><br>
![Screenshot (391)](https://user-images.githubusercontent.com/48363834/85943262-9f54a880-b94c-11ea-8ee3-2fa65fc7a9f7.png)
![Screenshot (392)](https://user-images.githubusercontent.com/48363834/85943273-ac719780-b94c-11ea-9a83-4481262611f0.png)

After launching jenkins:
**3. Create a job chain of job1, job2, job3 and  job4 using build pipeline plugin in Jenkins**

**4.  Job1 : Pull  the Github repo automatically when some developers push repo to Github.**<br><br>
![2](https://user-images.githubusercontent.com/48363834/85943338-125e1f00-b94d-11ea-87db-f8a00e6ad189.PNG)
![3](https://user-images.githubusercontent.com/48363834/85943342-1427e280-b94d-11ea-91de-868285921fcc.PNG)


**5.  Job2 : By looking at the code or program file, Jenkins should automatically start the respective language interpreter install image container to deploy code ( eg. If code is of  PHP, then Jenkins should start the container that has PHP already installed ).**<br><br>
![5](https://user-images.githubusercontent.com/48363834/85943406-84366880-b94d-11ea-808b-33a2e2a8337c.PNG)
![6](https://user-images.githubusercontent.com/48363834/85943410-86002c00-b94d-11ea-9755-b83acbcc571b.PNG)


**6. Job3 : Test your app if it  is working or not.**<br><br>
![7](https://user-images.githubusercontent.com/48363834/85943444-ca8bc780-b94d-11ea-86b6-892dfdad8968.PNG)

**7. Job4 : if app is not working , then send email to developer with error messages.**<br><br>
![8](https://user-images.githubusercontent.com/48363834/85943527-38d08a00-b94e-11ea-80aa-53616aeab159.PNG)

If any failure occur a mail will be send to developer like this:<br><br>
![WhatsApp Image 2020-06-28 at 14 46 10](https://user-images.githubusercontent.com/48363834/85943529-3b32e400-b94e-11ea-98e8-acb20e48ef44.jpeg)

### Build Pipeline:<br><br>
![e](https://user-images.githubusercontent.com/48363834/85943573-8220d980-b94e-11ea-8112-f52eba843914.PNG)

**8. Create One extra job job5 for monitor : If container where app is running. fails due to any reson then this job should automatically start the container again.**<br><br>
![4](https://user-images.githubusercontent.com/48363834/85943618-d035dd00-b94e-11ea-93bf-d0f54bc8d5b9.PNG)

**_Thank You!!_**


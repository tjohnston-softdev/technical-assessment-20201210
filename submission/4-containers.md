# Chapter 4 - Containers

---

### What is Webpack and why would it be used in a project?

'Webpack' is essentially a complier for JavaScript-based projects similar to compliers for other languages including C. It is a tool that is used to bundle all of the project's assets (libraries, code, etc) into a single file (similar to an .exe file for desktop programs)

One of the benefits of using Webpack is that it gives you control over which assets should be incorporated into the local package and which ones should be downloaded on runtime. In turn, this allows you to fine-tune the size of the final product, bandwidth consumption on the client-side, and overall loading times.

---

### What command would you use to see a list of all the docker containers that you currently have on your local machine?

`docker ps`

---

### What command would you use to pull down the latest mongo container from Docker hub?

`docker pull mongo`

---

### What command would you use to run that mongo container locally and have it accessible on port 27017?

`docker run -d  --name mongo-example  -p 27888:27017`

---

[Return to Index](../readme.md)

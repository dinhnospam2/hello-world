# Load balancer
- What is it?
    - A load balancer is a device that acts as a **reverse proxy** and **distributes network** or application traffic across a number of servers. 
    - Load balancers are **used to increase capacity** (concurrent users) and **reliability of applications**. 
- Where it located?
    - Layer 4: Transport layer(IP, TCP, FTP, UDP)
    - Layer 7: Application layer(HTTP)
- Why we use?
    - They improve the overall performance of applications by decreasing the burden on servers associated with managing and maintaining application and network sessions, as well as by performing application-specific tasks.

# Nginx

- What is it?

    ![alt text](https://image.slidesharecdn.com/lcu14-lightningtalk-nginx-140929145834-phpapp02/95/lcu14-lightning-talk-nginx-4-638.jpg?cb=1412002741 "Nginx")
    -  **a free open source web server** which launch in 2004.
    -  one of a handful of servers written to solve the C10K problem(handle 10 000 connection)
    -  uses a much more scalable event-driven (asynchronous) architecture
- Who invented?
    -  Igor Sysoev, a Russian software engineer.
- What about the architecture?
    ![alt text](https://image.slidesharecdn.com/lcu14-lightningtalk-nginx-140929145834-phpapp02/95/lcu14-lightning-talk-nginx-6-638.jpg?cb=1412002741 "Logo Title Text 1")

- How does it work?
    - Apache uses one thread per request, whereas nginx is event-driven
    - The **master process** performs the privileged operations such as reading configuration and binding to ports, and then creates a small number of **child processes** (the next three types).
    - The **cache loader** process runs at startup to load the disk‑based cache into memory, and then exits. It is scheduled conservatively, so its resource demands are low.
    - The **cache manager** process runs periodically and prunes entries from the disk caches to keep them within the configured sizes.
    - The **worker processes** do all of the work! They handle network connections, read and write content to disk, and communicate with upstream servers.


- Why it use single thread?
 ?????

# References:
[Load balancer](https://f5.com/glossary/load-balancer)
[Nginx](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
[3](https://anturis.com/blog/nginx-vs-apache/)




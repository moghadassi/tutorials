# 🚀 Docker Stacks

Docker is a powerful tool for containerizing applications, but real-world applications are rarely made of just **one** service.  
They usually need multiple components working together — for example:

- A **Backend** (API or web server)
- A **Database** (to store information)
- A **Frontend** (user interface)

Managing all of these containers separately can be tricky.  
This is where **Docker Stacks** come in!

---

## ✨ What is a Docker Stack?

A **Stack** is a collection of services (containers) that run together as a single project.  
Think of it as a **team of containers** working side by side.  

Instead of starting containers one by one, you define them in a configuration file and deploy them together with a single command.  

---

## 🛠️ How to Use Docker Stacks

### 1. Create a `docker-compose.yml` file
Here is a simple example:

```yaml
version: "3.9"
services:
  web:
    image: nginx
    ports:
      - "80:80"

  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: example
```

This file describes two services:
- **web** → uses Nginx and exposes port 80  
- **db** → runs MySQL with a root password

---

### 2. Deploy the stack

Run the following command:

```bash
docker stack deploy -c docker-compose.yml mystack
```

- `-c` specifies the Compose file.  
- `mystack` is the name of the stack.  

Docker will automatically start all the services and connect them together.

---

### 3. Manage your stack

- List all stacks:

```bash
docker stack ls
```

- List services in a stack:

```bash
docker stack services mystack
```

- Remove a stack:

```bash
docker stack rm mystack
```

---

## 💡 Why Use Stacks?

- Run multiple services together  
- Simplify deployment in production (especially with Docker Swarm)  
- Scale services up or down easily  
- Keep your project organized with one configuration file  

---


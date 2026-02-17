# CST8915 Lab 4: Introduction to Docker

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## 1.Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=hJjYB5UZErg)

---

## 2.Reflection Questions

### i.What are the main differences between a Docker image and a Docker container?

A container is an isolated environment in which applications run. A container image is a read only image that is used as a template to launch a container. But container images become containers at runtime.

### ii.Explain how Docker's layered architecture improves efficiency.

The different images can share the same base layers, which saves a lot of storage space. Also, when we update the code, Docker only needs to rebuild the changed layer, not the whole image. This makes downloading and deploying applications much faster

### iii.Why does each container get its own writable layer?

- **Isolation:** Each container needs its own space to write data or change files without affecting other containers.
- **Efficiency:** the bottom image layers are read-only, they are shared by all containers. Adding a thin writable layer on top is very fast and saves a lot of disk space.


### iv.What are the benefits of using Docker Compose over running containers individually?

Running containers individually requires typing many long commands for each one, but you can start, stop, and rebuild all your services at once using one command by using Docker Compose. All settings for the environment are saved in one YAML file. And Docker Compose automatically creates a private network for all containers defined in the file.

---

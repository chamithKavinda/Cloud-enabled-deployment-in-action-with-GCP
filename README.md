# Enterprise Cloud Architecture - Practical Assignment

<p align="left">
  <strong>Chamith Kavinda</strong><br>
  Student ID: <code>2301682028</code><br>
  Email: <a href="mailto:chamith13kavinda@gmail.com">chamith13kavinda@gmail.com</a>
</p>

> **Cloud-Deployment-in-Action** - A hands-on guide to designing and deploying cloud-ready microservices with GCP.
> Covers Spring Boot backends with MySQL & MongoDB, a React + TypeScript frontend, and extensible media storage (local disk → S3/MinIO).

 This repository contains four projects:

- course-service (Spring Boot + MySQL)
- student-service (Spring Boot + MongoDB)
- media-service (Spring Boot + Local file storage, can be extended to S3/MinIO)
- frontend-app (React + TypeScript)

## 🎥 Video Demonstration

Watch the screen recording here: [Video Link](https://drive.google.com/file/d/1eTmWtNjCCIuIXvM3wMUJ7grOm2sPjIe5/view?usp=sharing)

## Backend Services

### 1. course-service
- Entity: Course(id, name, duration)
- Endpoints:
  - GET /courses
  - GET /courses/{id}
  - POST /courses
  - DELETE /courses/{id}
- Default port: 8081
- Configure MySQL settings

### 2. student-service
- Document: Student(registrationNumber, fullName, address, contact, email)
- Endpoints:
  - GET /students
  - GET /students/{id}
  - POST /students
  - DELETE /students/{id}
- Default port: 8082
- Configure MongoDB settings

### 3. media-service
- Resource: files
- Endpoints:
  - POST /files (multipart/form-data: file)
  - GET /files (list)
  - GET /files/{id} (fetch)
  - DELETE /files/{id} (delete)
- Default port: 8083
- Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`).

## Frontend (frontend-app)
- React + TypeScript + MUI + Axios + Vite app with 3 sections: Courses, Students, Media
- Scripts:
  - npm run dev (Vite dev server)
  - npm run build (TypeScript build + Vite build)
  - npm run preview (Preview built app)

## Build

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.

## License

This project is licensed under the **MIT License** - see the [LICENSE](https://github.com/chamithKavinda/Cloud-enabled-deployment-in-action-with-GCP/blob/master/LICENSE) file for details.

---

## Contact

For questions or support, please contact:

- **Name**: Chamith Kavinda  
- **Email**: chamth13kavinda@gmail.com  
- **GitHub**: [Chamith Kavinda](https://github.com/chamithKavinda)

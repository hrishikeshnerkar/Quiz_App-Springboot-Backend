# 📚 QuizApp Backend

A simple Spring Boot-based backend application for managing quizzes and questions. This project was built to understand the basics of Spring Boot, REST APIs, and JPA.

---

## 🚀 Features

- Add and retrieve quiz questions  
- Filter questions by category  
- Create quizzes with random questions  
- Retrieve quiz questions by quiz ID  
- Submit quiz responses and calculate score  

---

## 🛠️ Technologies Used

- Java 17+  
- Spring Boot  
- Spring Data JPA  
- MySQL Database  
- Lombok  

---

## 📦 API Endpoints

### 🔹 Question APIs (`/question`)
- `GET /allQuestions` – Get all questions  
- `GET /category/{category}` – Get questions by category  
- `POST /add` – Add a new question  

### 🔹 Quiz APIs (`/quiz`)
- `POST /create?category={category}&numQ={num}&title={title}` – Create a quiz  
- `GET /get/{id}` – Get quiz questions by quiz ID  
- `POST /submit/{id}` – Submit quiz responses and get score  

---

## 🧪 Models

- `Question`: Stores question details including options and correct answer  
- `Quiz`: Stores quiz metadata and associated questions  
- `QuestionWrapper`: Used to send questions without revealing correct answers  
- `Response`: Used to submit answers for evaluation  

---

## ⚙️ How to Run

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/quizapp-backend.git
   cd quizapp-backend
   ```
2. **Configure MySQL Database**
  Make sure MySQL is running and create a database named quizapp.
  Update application.properties with your credentials:
  ```bash
  spring.datasource.url=jdbc:mysql://localhost:3306/quizapp
  spring.datasource.username=root
  spring.datasource.password=root
  spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
  
  spring.jpa.hibernate.ddl-auto=update
  spring.jpa.show-sql=true
  spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
  ```
3. **Build the project**
   ```bash
   npm clean install
   ```
4. **Run the application**
   ```bash
   mvn spring-boot:run
   ```


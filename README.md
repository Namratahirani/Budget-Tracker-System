**Budget Tracker System**  

**Overview**  
The Budget Tracker System is a user-friendly Java application with a graphical user interface (GUI) built using **Java Swing**. It helps users manage their finances effectively by allowing them to set budgets, track expenses across different categories, and manage multiple accounts such as cash and cards. The system uses JDBC (Java Database Connectivity) to connect and interact with a relational database for secure and efficient data management.  

Features  
1.**User Registration and Login**:  
   - New users can register using their email.  
   - Existing users can log in to access their personalized dashboard.  

2.**Dashboard**:  
   - View and manage financial data in a structured layout.  

3.**Budget Management**:  
   - Set a monthly or weekly budget.  

4. **Expense Tracking**:  
   - Record expenses and categorize them (e.g., Food, Shopping, Bills, etc.).  
   - View categorized expenses for better insights.  

5. **Account Management**:  
   - Add multiple accounts such as cash, credit cards, or bank accounts.  
   - Track expenses for each account separately.  

6. **Database Integration**:  
   - **JDBC** ensures seamless interaction between the application and the relational database.  
   - User information, budgets, and expenses are stored persistently.  

---

## Installation and Setup  

### Prerequisites  
- **Java JDK 8 or higher** installed on your system.  
- A Java IDE (e.g., IntelliJ IDEA, Eclipse, or NetBeans) or a terminal for execution.  
- A relational database such as **MySQL**, **PostgreSQL**, or **SQLite**.  
- **JDBC driver** for your database (e.g., MySQL Connector/J for MySQL).  

### Steps to Run the Application  
1. Clone the repository or download the project files:  
   ```bash  
   git clone https://github.com/your-repo/budget-tracker.git  
   cd budget-tracker  
   ```  
2. Set up the database:  
   - Create a database (e.g., `budget_tracker_db`).  
   - Run the provided SQL script (`schema.sql`) to create necessary tables.  
3. Configure the database connection:  
   - Open the `DatabaseConnection.java` file in the `utils` package.  
   - Update the following fields with your database details:  
     ```java  
     String DB_URL = "jdbc:mysql://localhost:3306/budget_tracker_db";  
     String USER = "your-username";  
     String PASSWORD = "your-password";  
     ```  
4. Open the project in your preferred Java IDE.  
5. Run the `BudgetTrackerMain.java` file to start the application.  

---

## How to Use  

### Registration and Login  
- Launch the application.  
- Register with your email and password or log in to access your dashboard.  

### Budget Management  
- Navigate to the **Set Budget** section.  
- Enter your budget amount and save it to the database.  

### Adding an Expense  
- Go to the **Add Expense** section.  
- Fill in details such as amount, category, and account type (e.g., Card or Cash).  
- Save the expense to update your records in the database.  

### Viewing Expenses  
- Check your expense summary categorized by type and account.  

---

## Project Structure  
```
BudgetTracker/  
├── src/  
│   ├── models/            # Data models like User, Expense, Account  
│   ├── views/             # GUI components (Java Swing files)  
│   ├── controllers/       # Event handlers and application logic  
│   ├── utils/             # Utility classes, including DatabaseConnection  
│   └── sql/               # Database schema and SQL scripts  
├── resources/             # Assets like icons and styles  
└── README.md              # Documentation  
```  

---

## Technologies Used  
- **Java**: Core programming language.  
- **Java Swing**: For GUI development.  
- **JDBC**: For database connectivity.  
- **MySQL (or your database choice)**: For persistent data storage.  

---

## Database Details  
### Tables  
1. **Users**:  
   - `id` (Primary Key)  
   - `email`  
   - `password`  

2. **Budgets**:  
   - `id` (Primary Key)  
   - `user_id` (Foreign Key)  
   - `amount`  
   - `start_date`  
   - `end_date`  

3. **Expenses**:  
   - `id` (Primary Key)  
   - `user_id` (Foreign Key)  
   - `category`  
   - `amount`  
   - `account_type`  
   - `date`  

---





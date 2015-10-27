How to setup JDBC for Postgresql
================================
1. Download the Postgresql JDBC driver [here](https://jdbc.postgresql.org/download.html)
2. Add a `lib` folder to your Eclipse project. Your folder structure should be  

  ```
  my-project
  |
  |-- src
  |-- lib
  ...
  ```
3. Add the JDBC driver to your build path.
  1. Open your project in Eclipse. If it is already open, refresh it by right-clicking the project folder and clicking `Refresh`.
  2. Project - Properties - Java Build Path - Libraries (tab) - Add JARs - {choose the JAR from the `lib` folder}.
4. In your code, add  

  ```java
  Class.forName("org.postgresql.Driver");
  String url = "jdbc:postgresql://dbteach2.cs.bham.ac.uk/xyz123";
  Connection conn = DriverManager.getConnection(url, USERNAME, PASSWORD);
  ```
  Replace `USERNAME` and `PASSWORD` with your username and password, respectively.
5. Make sure you are connected to the VPN and run your code to see if you can connect.

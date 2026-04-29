1. Install Maven

```bash
sudo apt update
sudo apt install maven -y
```

Verify installation:

```bash
mvn -version
```
![check maven version](mavenversion.png)


2.Clone your application

```bash
git clone https://github.com/Ibrahim-Adel15/build2.git
```

3. Run Unit Tests

```bash
mvn test
```

![Checking unit tests to run](maventest.png)

4. Build the Application

```bash
mvn clean package
```
output: target/demo-0.0.1-SNAPSHOT.jar

To check run 
```bash
tree
```
![Directory structure tree](tree.png)

5. Run the Application

```bash
java -jar /target/hello-ivolve-1.0-SNAPSHOT.jar
```
output shall be : Hello Ivolve Trainee

![App Output](image.png)
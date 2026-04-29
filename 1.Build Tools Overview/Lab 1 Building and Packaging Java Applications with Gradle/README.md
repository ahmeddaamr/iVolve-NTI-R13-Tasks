1. Install Gradle

```bash
sudo apt update
sudo apt install gradle -y
```

Verify installation:

```bash
gradle -version
```
![check gradle version](gradleversion.png)


2.Clone your application

```bash
git clone https://github.com/Ibrahim-Adel15/build1.git
```

3. Run Unit Tests

```bash
gradle test
```
![applying unit test](test_result.png)

-------------------------------------------------
DISCLAIMER: if you witnessed this error
![build error](build_error.png)

change the following code in build.gradle
![build.gradle before change](build-gradle-before.png)
![build.gradle after change](build-gradle-after.png)

-------------------------------------------------

4. Build the Application

```bash
gradle build
```
![gradle build successful](build.png)

To check run 
```bash
tree
```
![Directory structure tree](tree.png)

5. Run the Application

```bash
java -jar build/libs/ivolve-app.jar
```
output shall be : Hello Ivolve Trainee

![App Output](test_result.png)
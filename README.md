# 🚀 Build Automation of Java Application Using Maven

## 📌 Project Overview

This project demonstrates **build automation of a Java application using Apache Maven**.  
It automates compilation, dependency management, testing, packaging, and artifact generation using Maven's standard build lifecycle.

This project simulates a real-world DevOps workflow used in enterprise environments.

---

## 🎯 Objective

- Automate the Java build process using Maven
- Understand and configure `pom.xml`
- Manage external dependencies
- Execute Maven lifecycle phases
- Generate a JAR build artifact
- Push project securely to GitHub using SSH

---

## 🛠️ Technologies Used

- Java 17
- Apache Maven 3.9.x
- Git
- GitHub (SSH Authentication)
- Visual Studio Code

---

## 📂 Project Structure

```
maven-demo/
│
├── src/
│   ├── main/java/com/internship/App.java
│   └── test/java/com/internship/AppTest.java
│
├── pom.xml
├── README.md
└── target/
```

---

## 📄 pom.xml Configuration

The `pom.xml` (Project Object Model) file is the core configuration file of a Maven project.

It defines:
- Project metadata
- Dependencies
- Build lifecycle behavior
- Plugins

### 🔹 Dependency Added

```xml
<dependency>
    <groupId>org.apache.commons</groupId>
    <artifactId>commons-lang3</artifactId>
    <version>3.14.0</version>
</dependency>
```

This dependency allows usage of the `StringUtils` class for advanced string manipulation.

---

## 💻 Application Code (App.java)

```java
package com.internship;

import org.apache.commons.lang3.StringUtils;

public class App {
    public static void main(String[] args) {
        String name = "aaditya";
        System.out.println("Capitalized Name: " + StringUtils.capitalize(name));
    }
}
```

---

## 🔄 Maven Build Lifecycle

When running the following command:

```
mvn clean install
```

Maven executes these phases automatically:

1. **clean** → Deletes previous build files (`target` folder)
2. **compile** → Compiles `.java` files into `.class`
3. **test** → Runs unit tests
4. **package** → Creates a JAR file
5. **install** → Installs the JAR into local Maven repository (`.m2`)

---

## ▶️ How To Run This Project

### Step 1: Clone the Repository

```
git clone git@github.com:YOUR_USERNAME/maven-build-automation.git
cd maven-build-automation
```

### Step 2: Build the Project

```
mvn clean install
```

Expected output:

```
BUILD SUCCESS
```

### Step 3: Run the Application

```
java -cp target/maven-demo-1.0-SNAPSHOT.jar com.internship.App
```

Expected output:

```
Capitalized Name: Aaditya
```

---

## 📦 Generated Build Artifact

After successful build, the artifact is generated at:

```
target/maven-demo-1.0-SNAPSHOT.jar
```

This JAR file is the final deployable output of the application.

---

## 🔐 GitHub SSH Authentication Setup

SSH authentication was configured to securely push code to GitHub.

### Steps Performed:

1. Generated SSH key:
   ```
   ssh-keygen -t ed25519
   ```

2. Added public key to GitHub:
   GitHub → Settings → SSH and GPG Keys

3. Verified authentication:
   ```
   ssh -T git@github.com
   ```

4. Updated remote to SSH:
   ```
   git remote set-url origin git@github.com:USERNAME/maven-build-automation.git
   ```

---

## 📚 Key Learning Outcomes

- Understanding Maven architecture
- Managing dependencies using Maven Central Repository
- Executing Maven lifecycle phases
- Generating reproducible builds
- Handling compilation errors
- Configuring SSH authentication for secure Git operations
- Using Git for version control

---

## 🏗️ DevOps Relevance

This project reflects real-world DevOps practices where:

- Builds are automated
- Dependencies are centrally managed
- Artifacts are generated automatically
- Projects are version-controlled
- Secure authentication is configured

Maven is commonly used in CI/CD pipelines with tools like Jenkins and GitHub Actions.

---

## 🏆 Conclusion

This project successfully demonstrates how Apache Maven simplifies Java build automation and dependency management.

It provides hands-on experience with:

- Project structuring
- Automated build lifecycle
- Artifact generation
- Secure GitHub integration

This reflects practical DevOps and software engineering workflows used in enterprise environments.

---

## 👨‍💻 Author

Aaditya Mourya  
DevOps & Cloud Computing Intern

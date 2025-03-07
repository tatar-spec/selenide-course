# 🚀 Selenide Course – Web Testing Like a Pro

Welcome to the **Selenide Course**! This repository contains test automation examples using **Selenide**, a powerful and concise framework built on top of Selenium WebDriver. If you like **flaky tests**, **timeouts**, and **boilerplate code**, this repo is NOT for you. 😆

![QA Life](https://media.giphy.com/media/l3q2K5jinAlChoCLS/giphy.gif)

---

## 📌 What’s Inside?

Selenide makes automated testing **easy, readable, and reliable**. Here, you’ll find various test scenarios showcasing its capabilities.

---

### 📂 Project Structure:

selenide-course/ │── src/ │ ├── test/java/ │ │ ├── github/ │ │ │ ├── BestContributorToSelenide.java │ │ │ ├── ConfigurationParameters.java │ │ │ ├── DragAndDrop.java │ │ │ ├── SelenideRepositorySearch.java │ │ ├── selenide/ │ │ │ ├── Snippets.java │── src/test/resources/ │ ├── readme.txt │── build.gradle │── gradlew │── gradlew.bat


---

### 🔍 Key Test Classes:

- **`BestContributorToSelenide.java`** – Verifies that **Andrei Solntsev** is the top contributor to Selenide’s GitHub repo.
- **`ConfigurationParameters.java`** – Tests configuration settings dynamically.
- **`DragAndDrop.java`** – Automates the **drag-and-drop** functionality.
- **`SelenideRepositorySearch.java`** – Searches for `selenide/selenide` on GitHub and ensures it's at the top.
- **`Snippets.java`** – Handy Selenide snippets for reference.

---

## 🎯 Getting Started

### **Requirements:**
- **Java 11+** ☕
- **Gradle** 📦
- **Chrome / Firefox / Edge** 🌎
- **WebDriver** (Automatically handled by Selenide)

---

### **Installation & Execution:**
1. **Clone the repository**:
   ```sh
   git clone https://github.com/yourusername/selenide-course.git
   cd selenide-course
   
2. **Run tests using Gradle**:
   ```sh
   ./gradlew test
  
3. **Run a specific test class**:
   ```sh
    ./gradlew clean test --tests github.BestContributorToSelenide
   
---

## 🔥 Code Examples
### 📌 GitHub Repository Search Test
   ```sh
@Test
void shouldFindSelenideRepositoryAtTheTop() {
    open("https://github.com/");
    $("[placeholder='Search GitHub']").setValue("selenide").pressEnter();
    $$("ul.repo-list li").first().$("a").click();
    $("#repository-container-header").shouldHave(text("selenide / selenide"));
  }

---

Expectation:

A Selenide fan searching for selenide/selenide on GitHub and seeing it at the top. 🏆

---
                
### Drag-and-Drop Test

```sh
@Test
void dragAndDrop() {
    open("https://the-internet.herokuapp.com/drag_and_drop");
    $("#column-a").shouldHave(exactText("A"));
    $("#column-b").dragAndDropTo("#column-a");
    $("#column-a").shouldHave(exactText("B"));
}

---

Expectation:

Works like magic! But wait… it doesn’t? 😱 Blame HTML5 Drag & Drop API.

---

🏆 Why Selenide?
Because WebDriver.wait() is for amateurs.
Because Thread.sleep() is for nightmares.
Because less code means fewer bugs.

Still using raw Selenium?

---

📚 Useful Resources
📖 Official Selenide Docs
💻 JUnit 5 Documentation
🔧 Gradle User Guide

---
                                              
🎉 **Happy Testing!** 🎉
🚀 Write tests like a boss, fail less, and debug less.


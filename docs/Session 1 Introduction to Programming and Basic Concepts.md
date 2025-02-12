**Objective:**  
By the end of this session, students will have set up their development environment using Anaconda and Dev C++, written their first Python and C++ programs, and gained an introduction to version control with Git and GitHub.

---

## Part 1: Setting Up Your Development Environment

### 1.1 Installing Python with Anaconda (15 minutes)

**Why Anaconda?**  
- **Simplified Installation:** Anaconda simplifies the installation of Python and its packages by bundling them together.
- **Package Management:** It includes tools like `conda` for managing packages and environments, making it easier to handle dependencies.
- **Integrated IDE:** Includes Jupyter Lab for writing and running Python code.

**Steps:**
1. **Download Anaconda:**
   - Go to the [Anaconda website](https://www.anaconda.com/products/distribution).
   - Choose the version appropriate for your operating system (Windows, macOS, or Linux) and download it.

2. **Install Anaconda:**
   - Run the installer and follow the instructions.
   - During installation, make sure to check the box to add Anaconda to your PATH (if available).

3. **Verify Installation:**
   - In your terminal(if Windows, use `Anaconda Prompt` in your program list; else, use the default terminal), you should be able to see the `(base)` like this(regardless the path on its right):![[_resources/Pasted image 20240816153330.png]]
   - run `jupyter lab` in your terminal, *Jupyter Lab will open in your web browser, where you can start writing and running Python code.*


**Interactive Task:**
- **Basic Python Program:** Open a new Jupyter notebook in Jupyter Lab and write the following code:

  ```python
  print("Hello, World!")
  ```

- **Save and Run:** Save the notebook as `hello_world.ipynb` and run the cell to see the output.
![[_resources/Pasted image 20240816160051.png]]

### 1.2 Installing Dev C++ (10 minutes)

**Why Dev C++?**  
- **Ease of Use:** Dev C++ provides a straightforward interface for beginners to write and run C++ programs.
- **Integrated Development Environment:** It includes all necessary tools in one package.

**Steps:**
1. **Download Dev C++:**
   - Go to the [Dev C++ website](https://sourceforge.net/projects/orwelldevcpp/).
   - Download the latest version of Dev C++.

2. **Install Dev C++:**
   - Run the installer and follow the prompts to complete the installation.

3. **Verify Installation:**
   - Open Dev C++ and create a new source file.

**Interactive Task:**
- **Basic C++ Program:** Write the following code in Dev C++:

  ```cpp
  #include <iostream>
  using namespace std;

  int main() {
      cout << "Hello, World!" << endl;
      return 0;
  }
  ```

- **Compile and Run:** Save the file as `hello_world.cpp`, compile, and run the program. (click like this:) ![[_resources/Pasted image 20240816155635.png]]
- you should be able to see a new window with text 'hello, world' in it.

---

## Part 2: First Challenge (15 minutes)

Use Python (and C艹) to print an ASCII artwork on the screen. For example:
```
 |\__/,|   (`\
 |_ _  |.--.) )
 ( T   )     /
(((^_(((/(((_/
```
or something huge(more difficult):
- [Hatsune Miku ASCII Art | Copy & Paste (emojicombos.com)](https://emojicombos.com/hatsune-miku-ascii-art)

Answer: [[Society/web dev courses/session 1 ans|session 1 ans]]

sth even more difficult: [USACO2015 Bronze Problem 2. Speeding Ticket](https://usaco.org/index.php?page=viewproblem2&cpid=568)

## Part 4: Introduction to Version Control with Git and GitHub

**Why Version Control?**  
- **Track Changes:** Manage code revisions and history.
- **Collaboration:** Work with others efficiently.

**Steps:**
1. **Install Git:**
   - Download from [Git's official website](https://git-scm.com/).
   - Install and verify by running `git --version` in your command prompt or terminal.

2. **Create a GitHub Account:**
   - Sign up at [GitHub](https://github.com/).

3. **Set Up a Repository:**
   - Create a new repository on GitHub.
   - Follow instructions to clone the repository and push your initial code.

**Interactive Task:**
- **GitHub Setup:** Show your GitHub account and successful Git installation to receive further instructions and finalize your setup.

*Once you've shown your setup, you can leave the classroom if you have completed the task.*

---

**End of Session 1**
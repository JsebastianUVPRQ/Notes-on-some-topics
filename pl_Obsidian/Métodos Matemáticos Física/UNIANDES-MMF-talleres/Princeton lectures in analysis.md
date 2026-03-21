1. Dé otra demostración de la fórmula de Jensen en el disco unitario usando las funciones (llamadas factores de Blaschke)  
   $$
   \psi_\alpha(z) = \frac{\alpha - z}{1 - \overline{\alpha}z}.
   $$  
   [Indicación: La función $f/(\psi_{z_1} \cdots \psi_{z_N})$ no se anula en ningún lado.]

2. Halle el orden de crecimiento de las siguientes funciones enteras:  
   (a) $p(z)$ donde $p$ es un polinomio.  
   (b) $e^{bz^n}$ para $b \neq 0$.  
   (c) $e^{e^z}$.

3. Muestre que si $\tau$ está fijo con $\text{Im}(\tau) > 0$, entonces la función theta de Jacobi  
   $$
   \Theta(z|\tau) = \sum_{n=-\infty}^{\infty} e^{\pi i n^2 \tau} e^{2\pi i n z}
   $$  
   es de orden 2 como función de $z$. Otras propiedades de $\Theta$ se estudiarán en el Capítulo 10.  
   [Indicación: $-n^2 t + 2n|z| \leq -n^2 t/2$ cuando $t > 0$ y $n \geq 4|z|/t$.]

4. Sea $t > 0$ dado y fijo, y defínase $F(z)$ mediante  
   $$
   F(z) = \prod_{n=1}^\infty (1 - e^{-2\pi n t} e^{2\pi iz}).
   $$  
   Obsérvese que el producto define una función entera de $z$.  
   (a) Muestre que $|F(z)| \leq Ae^{|z|^2}$, por lo tanto $F$ es de orden 2.  
   (b) $F$ se anula exactamente cuando $z = -int + m$ para $n \geq 1$ y $n, m$ enteros. Por lo tanto, si $\{z_n\}$ es una enumeración de estos ceros, se tiene  
   $$
   \sum \frac{1}{|z_n|^2} = \infty \quad \text{pero} \quad \sum \frac{1}{|z_n|^{2+\epsilon}} < \infty.
   $$  
   [Indicación: Para probar (a), escriba $F(z) = F_1(z)F_2(z)$ donde  
   $$
   F_1(z) = \prod_{n=1}^N (1 - e^{-2\pi n t} e^{2\pi iz}), \quad F_2(z) = \prod_{n=N+1}^\infty (1 - e^{-2\pi n t} e^{2\pi iz}).
   $$  
   Elija $N \approx c|z|$ con $c$ suficientemente grande. Entonces, puesto que  
   $$
   \left( \sum_{N+1}^\infty e^{-2\pi n t} \right) e^{2\pi |z|} \leq 1,
   $$  
   se tiene $|F_2(z)| \leq A$. Sin embargo,  
   $$
   |1 - e^{-2\pi n t} e^{2\pi iz}| \leq 1 + e^{2\pi |z|} \leq 2e^{2\pi |z|}.
   $$  
   Por lo tanto $|F_1(z)| \leq 2^N e^{2\pi N|z|} \leq e^{c|z|^2}$. Nótese que una variante simple de la función $F$ aparece como un factor en la fórmula del triple producto para la función theta de Jacobi $\Theta$, que se aborda en el Capítulo 10.]

5. Muestre que si $\alpha > 1$, entonces  
   $$
   F_\alpha(z) = \int_{-\infty}^\infty e^{-|t|^\alpha} e^{2\pi i z t} \, dt
   $$  
   es una función entera de orden de crecimiento $\alpha/(\alpha - 1)$.  
   [Indicación: Demuestre que  
   $$
   -\frac{|t|^\alpha}{2} + 2\pi |z||t| \leq c|z|^{\alpha/(\alpha-1)}
   $$  
   considerando los dos casos $|t|^{\alpha-1} \leq A|z|$ y $|t|^{\alpha-1} \geq A|z|$, para una constante $A$ apropiada.]

6. Pruebe la fórmula del producto de Wallis  
   $$
   \pi = \frac{2 \cdot 2}{1 \cdot 3} \cdot \frac{4 \cdot 4}{3 \cdot 5} \cdots \frac{2m \cdot 2m}{(2m-1) \cdot (2m+1)} \cdots
   $$  
   [Indicación: Use la fórmula del producto para $\sin z$ en $z = \pi/2$.]

7. Establezca las siguientes propiedades de los productos infinitos.  
   (a) Muestre que si $\sum |a_n|^2$ converge, entonces el producto $\prod (1 + a_n)$ converge a un límite no nulo si y solo si $\sum a_n$ converge.  
   (b) Halle un ejemplo de una sucesión de números complejos $\{a_n\}$ tal que $\sum a_n$ converja pero $\prod (1 + a_n)$ diverja.  
   (c) Halle también un ejemplo tal que $\prod (1 + a_n)$ converja y $\sum a_n$ diverja.

8. Pruebe que para todo $z$ el producto siguiente converge, y  
   $$
   \cos(z/2) \cos(z/4) \cos(z/8) \cdots = \prod_{k=1}^\infty \cos(z/2^k) = \frac{\sin z}{z}.
   $$  
   [Indicación: Use el hecho de que $\sin 2z = 2 \sin z \cos z$.]

9. Pruebe que si $|z| < 1$, entonces  
   $$
   (1 + z)(1 + z^2)(1 + z^4)(1 + z^8) \cdots = \prod_{k=0}^\infty (1 + z^{2^k}) = \frac{1}{1-z}.
   $$

10. Halle los productos de Hadamard para:  
    (a) $e^z - 1$;  
    (b) $\cos \pi z$ 
    [Indicación: Las respuestas son $e^{z/2} \prod_{n=1}^\infty (1 + z^2/4n^2\pi^2)$ y $\prod_{n=0}^\infty (1 - 4z^2/(2n+1)^2)$ respectivamente.]

11. Muestre que si $f$ es una función entera de orden finito que omite dos valores, entonces $f$ es constante. Este resultado sigue siendo válido para cualquier función entera y se conoce como el pequeño teorema de Picard.  
    [Indicación: Si $f$ evita $a$, entonces $f(z) - a$ es de la forma $e^{p(z)}$ donde $p$ es un polinomio.]

12. Suponga que $f$ es entera y nunca se anula, y que ninguna de las derivadas de orden superior de $f$ se anula nunca. Pruebe que si además $f$ es de orden finito, entonces $f(z) = e^{az+b}$ para algunas constantes $a$ y $b$.

13. Muestre que la ecuación $e^z - z = 0$ tiene infinitas soluciones en $mathbb{C}$.  
    [Indicación: Aplique el teorema de Hadamard.]

14. Deduzca del teorema de Hadamard que si $F$ es entera y de orden de crecimiento $\rho$ no entero, entonces $F$ tiene infinitos ceros.

15. Pruebe que toda función meromorfa en $\mathbb{C}$ es el cociente de dos funciones enteras. Además, si $\{a_n\}$ y $\{b_n\}$ son dos sucesiones disjuntas que no tienen límite finito ... (el enunciado está incompleto)

## NOW

# COURSERA
---
### 1### 1.

Question 1

A software development company is transitioning from a traditional waterfall model to a DevOps approach. Which of the following practices would be the most important to implement in order to foster a DevOps culture? Select the best answer.

 

D 

Promoting close collaboration and communication between development and operations teams throughout the software development lifecycle

Implementing strict deadlines for each stage of the development process to ensure timely completion

Adopting the latest automation tools without considering the specific needs and context of the company

Encouraging developers to focus solely on coding while the operations team handles deployment and maintenance

1 point

### 2.

Question 2

A team is developing a Python-based web application and wants to implement DevOps practices to accelerate their software delivery process. Which of the following strategies would contribute most significantly to achieving faster time to market? Select the best answer.

 

D 

Prioritizing large, infrequent releases with comprehensive feature sets to minimize disruption for users

Adopting CI/CD pipelines with automated testing at each stage to enable rapid iteration and frequent releases

Focusing primarily on manual testing procedures to ensure the highest level of quality control before each release

Assigning separate and distinct responsibilities to development and operations teams to maintain clear boundaries and minimize confusion

1 point

### 3.

Question 3

A software development team is facing challenges with frequent integration errors and delays in delivering new features. They are considering implementing CI/CD practices to address these issues. Which of the following best describes how CI/CD can help improve their development process? Select the best answer.

 

D 

CI/CD encourages developers to work in isolation and only merge code changes when features are fully completed.

CI/CD automates the build, test, and deployment process, enabling frequent code integration and faster feedback loops.

CI/CD promotes infrequent code integration to minimize conflicts and reduce the risk of introducing errors.

CI/CD allows developers to manually test and deploy code changes, ensuring thorough quality checks before release.

1 point

### 4.

Question 4

A development team wants to implement a monitoring system for their Python application to gain insights into its performance and identify potential issues. Which of the following best describes the roles of Prometheus and Grafana in such a system? Select the best answer.

 

D 

Prometheus visualizes performance metrics in real-time, while Grafana collects and stores the raw data.

Prometheus and Grafana both focus on collecting performance metrics, but Grafana provides more detailed historical analysis.

Prometheus collects and stores performance metrics, while Grafana transforms the data into interactive visualizations.

Prometheus is primarily used for setting alerts on performance metrics, while Grafana is used for long-term trend analysis.

1 point

### 5.

Question 5

A Python application is experiencing performance issues, and the development team suspects that certain database queries are causing bottlenecks. Which capabilities of logging and tracing would be most helpful in investigating and resolving these performance problems? Select all that apply.

 

D 

Logging and tracing can automatically optimize the database queries to improve performance without requiring code changes.

Tracing can capture the flow of execution between the application and the database, revealing any delays or inefficiencies in the interaction.

Logging can track the frequency of specific database queries, helping identify those that are being executed excessively.

Logging can record the execution time of database queries, helping identify those that are taking longer than expected.

1 point

### 6.

Question 6

A Python web application suddenly becomes unavailable to users. The development team initiates the incident response process. What is the primary goal of the triage phase in this situation? Select the best answer.

 

D 

Gather comprehensive user feedback to understand the impact of the outage on their experience.

Immediately implement a permanent solution to prevent the issue from reoccurring.

Conduct a detailed analysis of historical logs to identify the root cause of the outage.

Quickly assess the situation, classify the severity of the incident, and take initial steps to contain any further damage.

1 point

### 7.

Question 7

A software development team is struggling to meet deadlines due to a rigid, documentation-heavy process that slows down their progress. Which Agile Manifesto value would be most helpful in addressing this challenge? Select the best answer.

 

D 

Customer collaboration over contract negotiation

Individuals and interactions over processes and tools

Working software over comprehensive documentation

Responding to change over following a plan

1 point

### 8.

Question 8

A software development team is tasked with building a system for a highly regulated industry where strict compliance and documentation requirements are in place. The project scope is well-defined and stable, with little expectation of changes during development. Which methodology would be most suitable for this scenario? Select the best answer.

 

D 

Agile would be most suitable, due to its flexibility and adaptability to changing requirements.

A hybrid approach combining elements of both Agile and Waterfall would be most suitable, to balance flexibility and structure.

Neither Agile nor Waterfall would be suitable, as a more modern iterative methodology would be preferable.

Waterfall would be most suitable, due to its structured approach and emphasis on thorough documentation and upfront planning.

1 point

### 9.

Question 9

A software development team is working on a project with a fixed timeline and a detailed plan. However, they realize that some of the initial requirements were unclear and need to be adjusted. According to the Agile Manifesto, how should the team approach this situation? Select the best answer.

 

D 

Stick to the original plan to avoid disrupting the timeline, even if it means delivering a product that doesn't fully meet the client's needs.

Ignore the new information and continue developing the software based on the initial understanding of the requirements.

Welcome the changing requirements and adapt the plan accordingly, even if it means adjusting the timeline or scope of the project.

Negotiate a new contract with the client to accommodate the changes, potentially delaying the project significantly.

1 point

### 10.

Question 10

A company is considering adopting Agile practices to improve their software development process. They are particularly interested in achieving a faster return on investment (ROI) for their projects. How can Agile contribute to achieving this goal? Select the best answer.

 

D 

Agile encourages delaying releases until the product is perfect to avoid any negative feedback that could impact ROI.

Agile prioritizes extensive documentation and upfront planning to minimize the risk of changes and ensure a predictable ROI.

Agile emphasizes delivering working software in short iterations, allowing for early validation of product ideas and faster generation of revenue.

Agile focuses on delivering a complete and perfect product in a single, large release at the end of the development cycle, maximizing initial impact.

1 point

# Coursera 2

### 1.

Question 1

You're working on an e-commerce platform, and you need to store product information, including the product name, price, description, and availability. Which data structures would be suitable for handling this information, considering you might need to update product details and access them quickly? Select all that apply.

  

   

Set

Tuple

Dictionary

List

1 point

### 2.

Question 2

In a social media application, you need to implement features for managing user relationships. Which data structures would be suitable for storing friend lists, identifying mutual friends between two users, and recommending potential connections? Select all that apply.

  

   

Set

List

Heap

Deque

1 point

### 3.

Question 3

You are developing a program that needs to process tasks in a specific order, with the most recently added task being handled first. Which data structure would be best suited for managing these tasks? Select the best answer.

  

   

Queue

Stack

Heap

Deque

1 point

### 4.

Question 4

You are building a library with classes that need to be registered with a framework upon initialization. Which type of decorator would be most suitable for this task? Select the best answer.

  

   

Function decorator

Class decorator

Method decorator

Built-in decorator

1 point

### 5.

Question 5

You're working with a large dataset and need to process it efficiently without loading the entire dataset into memory. You decide to implement a function that reads and processes the data in chunks. Which concept would be most suitable for creating this memory-efficient function? Select the best answer.

  

   

Context manager

List comprehension

Generator

Decorator

1 point

### 6.

Question 6

A team of developers is building a complex application with multiple modules and intricate interactions. They want to gain insights into the application's behavior, track down bugs effectively, and monitor performance bottlenecks. Which techniques can help them achieve these goals? Select all that apply.

  

   

Use debugging tools and techniques, such as breakpoints and step-through execution, to examine the application's state during runtime.

Implement logging throughout the application to record important events, errors, and other relevant information.

Employ code profiling to analyze the performance of different parts of the application and identify areas for optimization.

Conduct thorough unit testing to ensure that individual components of the application function correctly in isolation.

1 point

### 7.

Question 7

A software development team is building a web application using a framework that employs metaclasses to automatically register classes with the URL routing system. What is the most likely benefit of this approach for the developers? Select the best answer.

  

   

Improved application performance

Increased code reusability

Reduced development time

Enhanced code readability

1 point

### 8.

Question 8

A software company is developing a framework for data analysis. They want to enable users to extend the framework's functionality by defining their own custom data processing operations. Which aspect of metaprogramming would be most relevant for achieving this goal? Select the best answer.

  

   

Using decorators to enforce specific data formatting rules

Monkey patching to modify the behavior of existing data analysis tools

Code generation to create fixed data analysis pipelines

Introspection to identify and integrate user-defined operations

1 point

### 9.

Question 9

A developer is working with a library that provides objects representing network connections. They need to determine if a particular connection object supports secure communication. Which introspection function would be most helpful in this scenario? Select the best answer.

  

   

getattr()

type()

hasattr()

dir()

1 point

### 10.

Question 10

In the context of an ORM, what is the primary function of a metaclass like the ORMMetaclass? Select the best answer.

  

   

To automate the creation of database tables based on model class definitions

To define the structure and behavior of individual objects within a class

To manage the connection and disconnection to the database

To streamline the mapping between model class attributes and database columns

1 point

### Coursera Honor Code

  [Learn more](https://learner.coursera.help/hc/articles/209818863)

# ACTIVITY

In this project, you practiced applying maintenance best practices to an automation script that fetches sports scores and record

s them in an Excel spreadsheet. You identified and resolved an IndexError caused by incorrect indexing of the today variable. By carefully reading the error message, examining the code, and correcting the indexing, you successfully ensured the script runs smoothly and accurately records data. This exercise reinforced the importance of troubleshooting techniques in maintaining and improving automated processes.

If you would like to view a solution file to this exercise, you can download it here:

[

](https://d3c33hcgiwev3.cloudfront.net/_11ec2f47f49f486397d463accf93b903_PYTC3M4P01_Activity_Maintenance_best_practices_in_action_SOLUTION.zip?Expires=1774117433&Signature=I3JYf0ZFI9NP45qXP1IsvwcdazB33ATYyVBFyCuEuK-Jb7mW-P3zKUYbmnoR787fbn4uUXrI0JlspEOIQAra8vRzt2HhoNVzgqyjILzo4lb8D4noBKIXgGab~xw3V91YxSLIlkH12KuFkAcSa9ShIL9PsxU9BAW4AOKhmp5KVy8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

### 1.

Question 1

If you were to alter this program to use the logging module, what logging level would you use to only log the most severe errors? Select the best answer.

     

      

DEBUG

WARNING

ERROR

CRITICAL

1 point

### 2.

Question 2

If this program was a high-priority task, what would be the best way to alert staff in real-time? Select the best answer.

     

      

SMS

Printing to the console

Log file

Email notification



# 1


Once you have your script working, you need to package it and its dependencies into a deployment package.

Let's package your Python script and its dependencies for deployment to Azure Functions. Think of this like packing a suitcase for a trip – you need to include everything essential for your code to run smoothly in its new cloud environment.

### Here's a breakdown of the process:

**1. Create a requirements.txt file:** This file lists all the external libraries your script needs. You can create it manually or use pip freeze > requirements.txt in your terminal to automatically generate it based on your current environment. For our image processing script, it should look something like this:

azure-storage-blob

Pillow

**2. Create a virtual environment (optional but recommended):** A virtual environment helps isolate your project's dependencies from your global Python environment. This is like packing a separate toiletry bag instead of throwing everything loosely into your suitcase – it keeps things organized and prevents conflicts.

- Open your terminal and navigate to your project directory.
    
- Create a virtual environment: python -m venv .venv (or use virtualenv .venv)
    
- Activate the environment:
    
    - On Windows: .venv\Scripts\activate
        
    - On macOS/Linux: source .venv/bin/activate
        

**3. Install dependencies:** With your virtual environment activated, use pip install -r requirements.txt to install all the required libraries.

**4. (For local development/testing) Create a zip file:** If you're testing locally or using a deployment method that requires a zip file, you can create one:

- Make sure your script (main.py in our case) and the requirements.txt file are in your project's root directory.
    
- From your project directory (with the virtual environment deactivated), run the following command in your terminal to create a zip file named my_function_app.zip:
    

Bash

zip -r my_function_app.zip.

### Important considerations for deployment:

- **Deployment method:** Azure Functions offers several deployment methods, including:
    
    - **Using the Azure portal:** You can upload your zip file directly through the portal.
        
    - **Using the Azure CLI:** You can use command-line tools to deploy from your local machine.
        
    - **Using continuous deployment:** You can set up automatic deployments from a source code repository (like GitHub or Azure DevOps).
        
- **Dependencies:** Ensure all dependencies are compatible with the Python version supported by your chosen Azure Functions runtime.
    
- **File structure:** Azure Functions expects a specific file structure. Make sure your main.py (or whatever you named your main function file) is in the root directory of your deployment package.
    
- **Function app settings:** You'll need to configure any necessary application settings, such as environment variables, in your function app's configuration in the Azure portal.
    

By following these steps, you'll have a neatly packaged deployment ready to be sent to Azure Functions. Let me know if you have any questions or want to explore specific deployment methods in more detail!

Next, you'll deploy the function to Azure.

You're ready to deploy! Let's get that image processing function up and running in Azure. Here's how you can deploy it using the Azure portal, which is a user-friendly way to get started.

### Deploying via the Azure portal

**1. Package your function:** If you haven't already, follow the steps I provided earlier to package your function code and its dependencies into a zip file (e.g., my_function_app.zip).

**2. Go to your function app:** In the Azure portal, navigate to the function app you created earlier.

**3. Deployment options:**

- On the left-hand menu, under "Deployment," you'll see several options. For this method, select "Upload from package."
    

**4. Upload your zip file:**

- Click the "Browse" button and select the zip file you created.
    
- Click the "Upload" button.
    

**5. Deployment progress:**

- Azure will start deploying your function. You can monitor the progress in the portal.
    

**6. Verify deployment:**

- Once the deployment is complete, you should see a success message.
    
- You can now test your function by sending an HTTP request to its URL (you can find the URL in the function's overview tab).
    

### Alternative deployment methods

While the Azure portal is convenient for initial deployments, you might want to explore other methods as you become more comfortable with Azure:

- **Azure CLI:** The Azure CLI provides command-line tools for deploying functions. This can be more efficient for automated deployments or if you prefer working in the terminal.
    
- **Continuous deployment:** You can set up continuous deployment from a source code repository like GitHub or Azure DevOps. This automates the deployment process whenever you update your code in the repository.
    

### Important notes

- **Deployment credentials:** Make sure you have the necessary permissions to deploy to the function app.
    
- **Application settings:** Configure any required application settings, such as environment variables, in your function app's configuration.
    
- **Monitoring:** After deploying, monitor your function's performance and logs in the Azure portal to ensure it's running smoothly.
    

With your function deployed, you're one step closer to having a fully functional image processing app!

We will now set up your Azure Function to spring into action whenever a new image lands in your storage account. It's like setting up a motion sensor that triggers a light – in this case, a new image "triggers" your resizing function.

Here's how you configure the trigger:

**1. Navigate to your function:** In the Azure portal, go to your Function App and select the specific function you created for image processing.

**2. Go to the "Integration" tab:** You'll find this tab at the top of your function's page, usually next to the "Code + Test" tab.

**3. Add a trigger:**

- Click the "+ Add" button under "Triggers."
    
- Select "Azure Blob Storage" as the trigger type.
    

**4. Configure the trigger:**

- **Blob path:** Specify the path within your storage container that you want to monitor for new images. You can use {name} to capture the file name of the uploaded blob, which your function can then use to access the image. For example, if you want to monitor the root of your "images" container, you would enter images/{name}.
    
- **Connection string setting:** Choose the storage account connection string you want to use. You can either use the default connection string for your function app or create a new one specifically for this trigger.
    
- **Event type:** Select "Blob created" to trigger the function when a new blob is uploaded.
    

**5. Save your changes:** Click "Save" to apply the trigger configuration.

### Testing the trigger

- **Upload an image:** Now, try uploading an image to the specified path in your storage container.
    
- **Monitor the function:** Go to the "Monitor" tab for your function. You should see an execution log entry indicating that the function was triggered and processed the image.
    
- **Check for the resized image:** Verify that the resized image appears in the designated location in your storage container.
    

### Important notes

- **Trigger limitations:** Be aware of the trigger's limitations, such as the maximum blob size it can handle.
    
- **Error handling:** Implement robust error handling in your function to gracefully handle any issues during image processing or storage interactions.
    
- **Security:** If your storage account requires authentication, ensure that your function has the necessary permissions to access the container.
    

By configuring this trigger, you've automated the image resizing process. Any new image uploaded to your storage account will now be automatically resized by your serverless function. This is a great example of how serverless computing can simplify and streamline common tasks!

To test your application, upload an image and verify that the resized version appears in the storage account.

In this activity, you learned how to build a serverless application on Azure that automatically resizes images when they're uploaded to cloud storage. You created an Azure Function, wrote a Python script to handle the resizing, and configured a trigger to activate the function whenever a new image is added to your storage container. This allowed you to experience firsthand the power and efficiency of serverless computing for automating tasks in the cloud.

### 1.

Question 1

What is the primary purpose of an Azure Function in the context of this activity?

      

    

To provide a web interface for users to upload images.

To store and manage images.

To manage the infrastructure and operating system for the application.

To trigger the resizing process when a new image is uploaded.

1 point

### 2.

Question 2

Which Python library is essential for interacting with Azure Blob Storage in this activity?

      

    

azure.storage.blob

requests

json

os

1 point

### 3.

Question 3

What are the key benefits of using serverless computing for this image processing application?

      

    

Reduced operational overhead.

Scalability.

Increased control over the underlying hardware.

Cost-effectiveness.

1 point

### 4.

Question 4

What is the purpose of the requirements.txt file in this activity?

      

    

To define the connection string for the Azure Storage account.

To store the code for the Azure Function.

To configure the trigger for the Azure Function.

To list the external Python libraries required by the function.

1 point

### 5.

Question 5

Which of the following steps are involved in deploying the function to Azure?

      

    

Configuring the function trigger in the Azure portal.

Uploading the function code to the Azure portal or using other deployment methods.

Manually installing the Azure Functions runtime on a virtual machine.

Packaging the function code and dependencies into a zip file.

# RESPONSIBLE

### 1.

Question 1

You're responsible for maintaining a critical automation script that handles daily database backups. Why is it important to incorporate error alerts into this script? Select the best answer.

       

    

To stop the script immediately on error

To improve the performance of the script

To notify administrators of issues promptly

To reduce the need for logging

1 point

### 2.

Question 2

You're developing an automation script to handle a critical task and want to implement a logging system to track its execution and identify any potential issues. Which of the following are key components that should be included in this logging system? Select all that apply.

       

    

Timestamp of events

Execution duration

System hardware specifications

User login credentials

1 point

### 3.

Question 3

You're automating a task that involves sending emails to a large number of customers. You want to ensure that the automation script remains responsive to other requests while sending emails, preventing it from becoming unresponsive or blocking other processes. What is the primary advantage of using asynchronous programming in this scenario? Select the best answer.

       

    

Improved performance

Simplified code structure

Reduced development time

Enhanced readability

1 point

### 4.

Question 4

You're working on a project that involves collecting large amounts of data from various websites. You need a Python library that can handle the challenges of large-scale distributed web scraping, including efficient task management, error handling, and data extraction. Which library would be the most suitable choice? Select the best answer.

       

    

pandas

Scrapy

BeautifulSoup

Requests

1 point

### 5.

Question 5

You have developed an automation testing script that mirrors a complete user journey. This script simulates browsing through a catalog of products, selecting desired items, adding them to the shopping cart, navigating to the checkout page, entering payment details, and finally, confirming the purchase. What type of automation testing is being performed? Select the best answer.

       

    

Integration testing

Test-driven development

Unit testing

End-to-end testing testing

1 point

### 6.

Question 6

You're developing a complex automation script that involves multiple components interacting with each other. You want to ensure that the entire script functions correctly from start to finish, including user interactions and data processing. What are the key benefits of using end-to-end testing in this scenario? Select all that apply.

       

    

Detects defects in the interaction between integrated components

Ensures that individual modules work in isolation

Validates the complete workflow of the application

Evaluates the application's performance under load

1 point

### 7.

Question 7

You're working on a Python script that processes large amounts of data, but you notice that it's running slower than expected. You want to optimize the script's performance to reduce the execution time. Which of the following methods would be most effective in achieving this? Select the best answer.

       

    

Utilizing efficient algorithms and data structures

Minimizing the use of list comprehensions

Avoiding the use of built-in functions

Using global variables wherever possible

1 point

### 8.

Question 8

You're working on a Python project and want to ensure that your code is efficient and performs well. Which of the following are considered best practices for writing efficient Python code? Select all that apply.

       

    

Using list comprehensions

Using large functions to handle multiple tasks

Minimizing the use of nested loops

Increasing use of input/output operations

1 point

### 9.

Question 9

You're analyzing a Python program that seems to be consuming an increasing amount of memory over time, even though it shouldn't be. You suspect a memory leak might be the cause. Which of the following scenarios is a common cause of memory leaks in Python? Select the best answer.

       

    

Circular references in data structures

Frequent context switching in multithreaded programs

Excessive use of built-in functions

Using large global variables

1 point

### 10.

Question 10

You're responsible for an automation script that handles critical tasks and needs to run reliably without interruption. What's the most effective way to ensure its continuous and reliable operation over time? Select the best answer.

       

    

By implementing automated testing and monitoring.

By manually checking the script operation periodically.

By avoiding updates to the script.

By minimizing the use of logging to reduce overhead.

# LAST

### 1.

Question 1

You're building a professional GitHub portfolio to showcase your skills and experience to potential employers. What language should you use to write your README file for a project?? Select the best answer.

     

      

HTML

Python

Markdown

Flask

1 point

### 2.

Question 2

You're working on a team project and you have encountered a conflict. What is the most likely cause? Select the best answer.

     

      

A failing test

A missing library

An error in your code

You and a team member have made changes to the same code in different branches

1 point

### 3.

Question 3

Which of the following are best practices when it comes to team communication? Select all that apply.

     

      

Document code

Code reviews only when necessary

Have regular check-ins with the team

Use active listening strategies

1 point

### 4.

Question 4

You're working on a collaborative project and encounter a merge conflict when trying to integrate changes from another branch. Which of the following Git commands can help you resolve this conflict? Select all that apply.

     

      

git push

git merge --abort

git add

git mergetool

1 point

### 5.

Question 5

You want to view the differences between two commits. Which git command can you use?? Select the best answer.

     

      

git log

git diff

git checkout

git reset

1 point

### 6.

Question 6

You have a series of extremely large data files you want to keep out of your repository. What is the best way to ensure you and your team do not store these files in Git? Select the best answer.

     

      

Create a branch for the data files

Hide the files using your operating system

Add the file names to the .gitignore file for the repository

Delete the files from your computer

1 point

### 7.

Question 7

You're working on a team project and have been using pull requests to handle code changes. Which of the following best describes the primary benefit of using pull requests on GitHub in this scenario? Select the best answer.

     

      

To automatically merge changes without any review.

To increase the storage capacity of the repository.

To facilitate discussion and review of code changes before merging.

To delete unwanted branches from the repository.

1 point

### 8.

Question 8

You're reviewing a colleague's code as part of a collaborative project. What should be your primary focus during this code review to ensure the code is high-quality and maintainable in the long run? Select the best answer.

     

      

Checking for compliance with company policies

Identifying and fixing syntax errors

Verifying the code runs without issues

Ensuring good code readability and structure

1 point

### 9.

Question 9

You're starting a new coding project with a team of developers and need to choose tools that will help facilitate collaboration and communication throughout the project. Which of the following tools would be suitable for this purpose? Select all that apply.

     

      

Microsoft Teams

Azure DevOps

Microsoft Word

GitHub

1 point

### 10.

Question 10

Why might a developer choose to rebase a project rather than merge? Select all that apply.

     

      

To create a cleaner, linear history

To simplify merge conflicts

To simplify the process of using the repository

To simplify the commit history

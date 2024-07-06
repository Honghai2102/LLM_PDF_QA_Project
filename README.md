# LLM-PDF-QA_Project 
## Deploy Chatbot using Ngrok

Ngrok is a handy tool that establishes a secure tunnel, allowing you to share your locally running chatbot with others for testing and interaction. Here's a step-by-step guide to deploying your chatbot using Ngrok:

### Step 1: Create a Ngrok Account

- Go to [Ngrok](https://ngrok.com/), create an account, and log in.

### Step 2: Get Your Authtoken

- Navigate to the **Your Authtoken** section and copy your authtoken.

### Step 3: Set Up Ngrok in Your Environment

- Open your development environment and install Ngrok by running the following command:
  ```python
  !pip install pyngrok -q


### Step 4: Configure Ngrok with Your Authtoken

- Run the following commands to configure Ngrok with your authtoken:
  ```python
  from pyngrok import ngrok

  !ngrok config add-authtoken YOUR_AUTHTOKEN
  ```


### Step 5: Deploy Your Application

- Run your application and start Ngrok to create a public URL:
  ```python
  public_url = ngrok.connect(8000).public_url
  ```

- Then run your application with Chainlit:
  ```bash
  !chainlit run app.py
  ```

### Step 6: Access Your Application

- Wait until the app.py finishes running (you will see a blue message saying "Your app is available at http://localhost:8000").
- Go to the public URL provided by Ngrok and see the result!


### Step7: "Instructions for using the website."
- After accessing the website, you proceed to upload a PDF file. Once the file has been uploaded, you can ask questions related to that file.

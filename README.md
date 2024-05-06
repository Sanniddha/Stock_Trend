# Stock-Market
- [Streamlit](https://streamlit.io/) is used to build the dynamic app. Streamlit is an open-source Python framework for data scientists and AI/ML developer to develop dynamic data apps with only a few lines of code
- [Neon](https://neon.tech/) database service is used for database management.
- [SendGrid](https://sendgrid.com/en-us/) is used to send email.

Create a file called ```secrets.toml``` in a folder called ```.streamlit``` at the root of your app repo and paste your secrets into that file.
Add your secrets in the "Secrets" field using the TOML format.
```
# .streamlit/secrets.toml
# Everything in this section will be available as an environment variable

DATABASE_URL="Paste Your PostgreSql Connection String Here"

SENDER_EMAIL="Paste the Sender Email Here"
EMAIL_HOST="smtp.sendgrid.net"
EMAIL_USERNAME="apikey"
EMAIL_PASSWORD="Paste the Generated Password Here"

HASH_SALT="Paste the Password Hash Key Here"
```

1. Create a folder (say `Stock_Project`).
2. [Clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository#cloning-a-repository) the repository inside the created folder. A new folder named `Stock_Market` will create inside the `Stock_Project` folder. 
3. Locate to `Stock_Project` folder/directory
   Open command terminal in this location and run the below command:
   ```
   python -m venv venv
   ```
   This command create a [virtual environment](https://realpython.com/python-virtual-environments-a-primer/) in your project folder.
5. Now run this command:
   ```
   .\venv\Scripts\activate
   ```
   This commnad activate your virtual environment
7. Now move to `Stock_Market` folder/directory using this command:
   ```
   cd Stock_Market
   ```
9. Now run this command:
   ```
   pip install -r requirements.txt
   ```
   This command install all necessary modules and there dependencies
11. Now run this commnad:
    ```
    streamlit run index.py --client.showSidebarNavigation=False
    ```
Now your appliaction is ready to use

When you are using the appliaction next time, you don't require to create the virtual environment and install the modules again. Just perform the following steps:
1. Locate to `Stock_Project` folder/directory
2. Open command terminal in this location and run the below command:
   ```
   .\venv\Scripts\activate
   ```
4. Now run this command:
   ```
   cd Stock_Market
   ```
6. Now run this command:
   ```
   streamlit run index.py --client.showSidebarNavigation=False
   ```


## References:
1. https://arxiv.org/abs/2111.15397
2. https://neuralprophet.com/science-behind/model-overview.html
3. https://ai.meta.com/blog/neuralprophet-the-neural-evolution-of-facebooks-prophet/
4. https://facebook.github.io/prophet/


# n8n Beginner Guide 🚀  

n8n is an open-source **automation and integration** tool that helps you connect services and APIs together and automate workflows without complex coding.  

---

## 1. Install n8n 🛠️  

There are several ways to install n8n, but here are the simplest ones:  

### Install with npm (for Node.js developers)  
```bash
npm install n8n -g
```

### Install with Docker (recommended)  
If you have Docker installed on your system:  
```bash
docker run -it --rm   -p 5678:5678   n8nio/n8n
```

After running, n8n will be available in your browser at:  
👉 [http://localhost:5678](http://localhost:5678)

---

## 2. First Run 🌐  

After starting n8n, you will enter the **Visual Workflow Editor**.  
Here you can drag and drop nodes to build your own workflow.  

---

## 3. Create Your First Workflow ⚡  

### Example: Fetch data from an API and send it to Telegram  

1. **Create a new Workflow**  
   From the main menu, click **New Workflow**.  

2. **Add an HTTP Request Node**  
   - Choose the `HTTP Request` node.  
   - Enter any API URL (e.g., [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts)).  

3. **Add a Telegram Node**  
   - Get your Bot Token from [BotFather](https://t.me/botfather).  
   - Add a `Telegram` node and connect it to the previous one.  
   - Send the fetched API data as a Telegram message.  

4. **Execute**  
   Click **Execute Workflow** and check the result in your Telegram. 🎉  

---

## 4. Save and Activate Workflows 💾  

- Use the **Save** button to store your workflow.  
- Use the **Activate** button if you want it to always run automatically.  

---

## 5. Useful Resources 📚  

- [Official Documentation](https://docs.n8n.io/)  
- [Community Forum](https://community.n8n.io/)  
- [n8n GitHub](https://github.com/n8n-io/n8n)  

---




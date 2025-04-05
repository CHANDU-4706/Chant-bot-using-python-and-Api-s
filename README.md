# Chat-bot-using-python-and-Api-s
This my intern project crated a chat bot using python and with the helf of api's data
Here are the **steps explaining how your ChatGPT terminal chatbot works**:

---

### **1. Import the OpenAI Library**
```python
import openai
```
- This loads the OpenAI Python package so you can use GPT models.

---

### **2. Set Your API Key**
```python
openai.api_key = "your-api-key"
```
- Authenticates your app with OpenAI’s API.  
- Best practice: use environment variables for security.

---

### **3. Initialize Chat**
```python
print("ChatGPT: Hi, I'm ChatGPT. I'm a helpful assistant")
```
- Shows a welcome message.

---

### **4. Set Up Initial Messages**
```python
messages = [{"role": "system", "content": "Hi ChatGPT, You are a helpful assistant!"}]
```
- Starts the chat with a system instruction to define the assistant’s behavior.

---

### **5. Get the First Bot Response**
```python
chat_completion = openai.ChatCompletion.create(model="gpt-3.5-turbo", messages=messages)
```
- Sends the first API call to get ChatGPT's initial reply.
- Appends the response to the `messages` list.

---

### **6. Start the Chat Loop**
```python
while True:
    message = input("👤: ")
```
- Runs an infinite loop waiting for user input.

---

### **7. Handle Special Commands**

- **`exit`**: ends the chat.
- **`clear`**: resets the conversation history and greets the user again.

---

### **8. Add User Message**
```python
messages.append({"role": "user", "content": message})
```
- Appends user input to the chat history.

---

### **9. Get ChatGPT's Response**
```python
chat_completion = openai.ChatCompletion.create(model="gpt-3.5-turbo", messages=messages)
reply = chat_completion["choices"][0]["message"]["content"]
```
- Sends a request to OpenAI’s API with the entire chat history.
- Gets ChatGPT's reply from the response.

---

### **10. Display Response**
```python
print(f"🤖: {reply}")
```
- Prints the bot’s reply to the terminal.

---

### **11. Loop Continues**
- The chat continues until the user types `exit`.

---

Let me know if you want a flow diagram or visual walkthrough too!

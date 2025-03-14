# 🌟 Stellar AI - Your Personalized Astrology Assistant
🚀 **Stellar AI** is an intelligent astrology app that generates personalized horoscopes, fortunes, and zodiac-based predictions. Built with **Kotlin, Jetpack Compose, and OpenAI API**, Stellar AI provides deep insights into astrological trends using AI-powered analysis.

🔮 Get your **daily horoscopes, astrology readings, and personalized cosmic insights** all in one place.

---

## 🔐 Firebase Authentication - Under the Hood

Stellar AI uses **Firebase Authentication** to securely manage user logins and sign-ups. Users can create accounts, log in with their credentials, and access personalized astrology insights.

### 🛠 What This Utilizes
- **🔥 Firebase Authentication** → Handles user sign-up, login, and session management.
- **📦 ViewModel & MutableStateFlow** → Manages authentication state and UI updates.
- **⚡ Kotlin Coroutines** → Executes authentication calls asynchronously.
- **🛠 Koin (Dependency Injection)** → Injects authentication services into ViewModels.
- **💾 Room Database** → Stores basic user data (e.g., zodiac sign, name, preferences).
- **🎭 Material 3 Components** → Ensures a clean and intuitive login/signup UI.
- **🖼️ Jetpack Compose UI** → Fully Compose-based authentication screens.

---

### 📜 How It Works
1️⃣ **User enters email and password** in the login form.  
2️⃣ **ViewModel triggers Firebase Authentication API** to validate credentials.  
   - If successful → User is authenticated and redirected to the main screen.  
   - If failed → An error message (e.g., "Authentication failed") is displayed.  
3️⃣ **Session state is managed** using Firebase's authentication listener.  
4️⃣ **User data is stored in Room Database** (name, zodiac sign, age, etc.) for personalized experiences.  
5️⃣ **On app restart, Firebase automatically restores session state**, keeping the user logged in.

---

### 🚀 Future Improvements
- 🔹 Implement **Google Sign-In & OAuth** for faster login options.
- 🔹 Add **email verification flow** for enhanced security.
- 🔹 Integrate **Biometric Authentication (Fingerprint/Face Unlock)** for a seamless experience.
- 🔹 Improve **error handling UX**, showing more detailed failure messages.

---
<img src="stellar_login_signup.gif" width="500"/>

---

## 💬 AI Chatbot - Under the Hood

The **Stellar AI Chatbot** allows users to interact with an **AI-powered astrology assistant**, generating responses to horoscope-related questions in real-time using the **OpenAI API**.

### 🛠 What This Utilizes
- **🤖 ChatGPT API (OpenAI + Retrofit)** → Processes user messages and generates intelligent responses.
- **📦 ViewModel & MutableStateFlow** → Manages chat history, user input, and API call state.
- **⚡ Kotlin Coroutines** → Ensures non-blocking, smooth API calls.
- **🛠 Koin (Dependency Injection)** → Injects API services and ViewModels efficiently.
- **📌 Room Database (Chat History)** → Stores previous conversations for session persistence.
- **🖼️ Jetpack Compose UI** → Dynamic chat UI with smooth animations.
- **🎭 Material 3 Components** → Ensures a polished, modern user experience.

---

### 📜 How It Works
1️⃣ **User types a question in the chat input field.**  
2️⃣ **ViewModel updates UI state** and triggers an **asynchronous API request** to OpenAI.  
3️⃣ **Loading state is displayed** while waiting for the API response.  
4️⃣ **ChatGPT API generates a response, which is processed and displayed** in the chat.  
5️⃣ **The response is stored in Room Database** (if caching is enabled).  
6️⃣ **User can continue the conversation** while previous messages remain visible.

---

### 🚀 Future Improvements
- 🔹 Implement **streaming responses** for real-time text generation.
- 🔹 Add **sentiment analysis** to tailor responses based on user tone.
- 🔹 Improve **error handling** with a **retry mechanism** for failed API calls.
- 🔹 Enable **voice input & text-to-speech** for a more interactive experience.

---

<img src="stellar_chat_bot.gif" width="500"/>

---

## 🔮 Fortunes Navigation - Under the Hood

The **Fortunes** feature provides AI-generated daily fortunes based on a user's zodiac sign. It integrates **ChatGPT API**, caches responses in a local database, and ensures a smooth, responsive UI experience.

### 🛠 What This Utilizes
- **🧭 Jetpack Compose Navigation** → Manages seamless screen transitions.
- **🤖 ChatGPT API (OpenAI + Retrofit)** → Fetches AI-generated daily fortunes.
- **⚡ Kotlin Coroutines & MutableStateFlow** → Handles asynchronous API calls and UI state updates efficiently.
- **📦 ViewModel & Custom UI State** → Centralized state management with `MutableStateFlow` for UI handling.
- **🛠 Koin (Dependency Injection)** → Injects dependencies like ViewModels, Room Database, and API services.
- **💾 Room Database** → Caches fortunes locally so users retrieve the same fortune for a given day.
- **🎨 Crossfade Animations** → Provides smooth UI transitions between loading and displaying the fortune.
- **🎭 Material 3 Components** → Ensures a polished, modern user experience.

---

### 📜 How It Works
1️⃣ **User selects the "Fortunes" feature** from the main menu.  
2️⃣ **ViewModel checks Room Database** for a cached fortune from today:  
   - If found → The stored fortune is displayed instantly.  
   - If not found → The app makes an **asynchronous API call** to ChatGPT.  
3️⃣ **The API response** is stored in Room Database for later access.  
4️⃣ **Fortune is displayed with a Crossfade animation** for a smooth transition.  
5️⃣ **On app restart, the same day’s fortune is retrieved from Room**, avoiding redundant API calls.

---

### 🚀 Future Improvements
- 🔹 Implement **Unit Tests** for API calls and database interactions.
- 🔹 Optimize **caching logic** to store multiple fortunes and user preferences.
- 🔹 Add **Retry Policy** for handling failed API calls gracefully.
- 🔹 Enhance **animations** for a more engaging user experience.

---

<img src="stellar_fortunes.gif" width="500"/>
****

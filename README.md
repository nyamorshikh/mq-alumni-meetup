<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="MQ Alumni AI Meet-Up - Professional development and networking for Macquarie University AI and analytics graduates" />
  <title>MQ Alumni AI Meet-Up</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    #bp-web-widget-container {
      z-index: 9999;
      position: fixed;
      bottom: 20px;
      right: 20px;
    }

    #chat-button {
      transition: transform 0.2s;
    }

    #chat-button:hover {
      transform: scale(1.1);
    }

    .chat-window {
      display: none;
      position: fixed;
      bottom: 100px;
      right: 20px;
      width: 350px;
      height: 500px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      z-index: 1000;
    }

    .chat-window.active {
      display: block;
    }

    @media (max-width: 400px) {
      .chat-window {
        width: 90%;
        right: 5%;
      }
    }
  </style>
</head>
<body class="bg-gray-100 font-sans">
  <!-- Header -->
  <header class="bg-blue-600 text-white py-6">
    <div class="container mx-auto px-4">
      <h1 class="text-4xl font-bold">MQ Alumni AI Meet-Up</h1>
      <p class="mt-2 text-lg">Empowering Macquarie University Alumni with AI-Driven Professional Development</p>
    </div>
  </header>

  <!-- Navigation -->
  <nav class="bg-gray-800 text-white py-3 sticky top-0 z-10">
    <div class="container mx-auto px-4">
      <ul class="flex flex-wrap space-x-6 justify-center">
        <li><a href="#home" class="hover:underline" aria-label="Home">Home</a></li>
        <li><a href="#services" class="hover:underline" aria-label="Services">Services</a></li>
        <li><a href="#chatbot" class="hover:underline" aria-label="Chatbot">Chatbot</a></li>
        <li><a href="#about" class="hover:underline" aria-label="About">About</a></li>
        <li><a href="#contact" class="hover:underline" aria-label="Contact">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- Main content -->
  <main class="container mx-auto px-4 py-8">
    <!-- Home Section -->
    <section id="home" class="mb-12">
      <h2 class="text-2xl font-bold mb-4">Welcome to the MQ Alumni AI Meet-Up</h2>
      <p class="mb-6">Join us for professional development and networking focused on AI and analytics.</p>
    </section>

    <!-- Services Section -->
    <section id="services" class="bg-white py-16 mb-12">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-8">Our Services</h2>
        <p class="text-center mb-10 max-w-3xl mx-auto">We offer tailored solutions to elevate your career, powered by our community and AI technology.</p>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
          <div class="bg-gray-100 p-6 rounded-lg shadow-md hover:shadow-lg transition">
            <h3 class="text-xl font-semibold mb-2">Personalized Answers</h3>
            <p>Our AI chatbot provides tailored recommendations for AI certifications, courses, and events, trained by our alumni community.</p>
          </div>
          <div class="bg-gray-100 p-6 rounded-lg shadow-md hover:shadow-lg transition">
            <h3 class="text-xl font-semibold mb-2">Mentorship Program</h3>
            <p>Connect with industry experts for 1:1 guidance to advance your career and master AI trends.</p>
          </div>
          <div class="bg-gray-100 p-6 rounded-lg shadow-md hover:shadow-lg transition">
            <h3 class="text-xl font-semibold mb-2">CV/Resume/LinkedIn Upgrades</h3>
            <p>Get AI-driven tips to optimize your professional profiles, tailored to your career goals.</p>
          </div>
          <div class="bg-gray-100 p-6 rounded-lg shadow-md hover:shadow-lg transition">
            <h3 class="text-xl font-semibold mb-2">Mock Interviews</h3>
            <p>Practice with AI-simulated interviews for your target role, complete with actionable feedback.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Chatbot Section -->
    <section id="chatbot" class="mb-12">
      <h2 class="text-2xl font-bold mb-4">Chatbot</h2>
      <p class="mb-6">Chat with our AI assistant for help and information about our services and events.</p>
    </section>

    <!-- About Section -->
    <section id="about" class="mb-12">
      <h2 class="text-2xl font-bold mb-4">About</h2>
      <p class="mb-6">Learn more about our mission to empower Macquarie University alumni through AI-driven professional development and networking.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="mb-12">
      <h2 class="text-2xl font-bold mb-4">Contact</h2>
      <form id="contact-form" class="max-w-lg mx-auto">
        <div class="mb-4">
          <label for="name" class="block text-sm font-medium text-gray-700">Your Name</label>
          <input type="text" id="name" placeholder="Your name" class="border p-2 rounded w-full focus:outline-none focus:border-blue-600" required />
        </div>
        <div class="mb-4">
          <label for="email" class="block text-sm font-medium text-gray-700">Your Email</label>
          <input type="email" id="email" placeholder="Your email" class="border p-2 rounded w-full focus:outline-none focus:border-blue-600" required />
        </div>
        <div class="mb-4">
          <label for="message" class="block text-sm font-medium text-gray-700">Your Message</label>
          <textarea id="message" placeholder="Your message" class="border p-2 rounded w-full h-32 focus:outline-none focus:border-blue-600" required></textarea>
        </div>
        <button type="submit" class="bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700">Send</button>
      </form>
    </section>
  </main>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white py-6">
    <div class="container mx-auto px-4 text-center">
      <p>© 2025 MQ Alumni AI Meet-Up. All rights reserved.</p>
      <p class="mt-2 text-sm">Committed to Responsible AI: Transparency, Fairness, Privacy.</p>
    </div>
  </footer>

  <!-- Chat Button -->
  <button id="chat-button" class="fixed bottom-6 right-6 bg-blue-600 text-white p-4 rounded-full shadow-lg hover:bg-blue-700 z-50" aria-label="Open chat">
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z" />
    </svg>
  </button>

  <!-- Chat Window -->
  <div id="chat-window" class="chat-window" role="dialog" aria-modal="true" aria-labelledby="chat-title">
    <div class="bg-blue-600 text-white p-4 rounded-t-lg flex justify-between items-center">
      <h3 id="chat-title" class="font-bold">MQ Alumni AI Assistant</h3>
      <button id="close-chat" class="text-white hover:text-gray-200" aria-label="Close chat window">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
    <div id="chat-messages" class="p-4 h-96 overflow-y-auto" tabindex="0" aria-live="polite">
      <!-- Messages will be inserted here -->
    </div>
    <div class="p-4 border-t">
      <div class="flex">
        <input type="text" id="chat-input" class="flex-1 p-2 border rounded-l-lg focus:outline-none focus:border-blue-600" placeholder="Type your message..." aria-label="Type your message" />
        <button id="send-message" class="bg-blue-600 text-white px-4 py-2 rounded-r-lg hover:bg-blue-700" aria-label="Send message">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
            <path d="M10.894 2.553a1 1 0 00-1.788 0l-7 14a1 1 0 001.169 1.409l5-1.429A1 1 0 009 15.571V11a1 1 0 112 0v4.571a1 1 0 00.725.962l5 1.428a1 1 0 001.17-1.408l-7-14z" />
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Scripts -->
  <script>
    // Form Submission
    document.getElementById('contact-form').addEventListener('submit', (e) => {
      e.preventDefault();
      alert('Thank you for your submission! This is a demo form. Join us via Meetup.com.');
      e.target.reset();
    });

    // Chat Functionality
    const chatButton = document.getElementById('chat-button');
    const chatWindow = document.getElementById('chat-window');
    const closeChat = document.getElementById('close-chat');
    const chatInput = document.getElementById('chat-input');
    const sendMessage = document.getElementById('send-message');
    const chatMessages = document.getElementById('chat-messages');

    // Toggle chat window
    chatButton.addEventListener('click', () => {
      chatWindow.classList.toggle('active');
      if (chatWindow.classList.contains('active')) {
        chatInput.focus();
      }
    });

    closeChat.addEventListener('click', () => {
      chatWindow.classList.remove('active');
      chatButton.focus();
    });

    // Send message function
    function sendChatMessage() {
      const message = chatInput.value.trim();
      if (message) {
        // Add user message
        const userMessage = document.createElement('div');
        userMessage.className = 'mb-4 text-right';
        userMessage.innerHTML = `
          <div class="inline-block bg-blue-600 text-white rounded-lg py-2 px-4 max-w-[70%]">
            ${message}
          </div>
        `;
        chatMessages.appendChild(userMessage);

        // Simulate bot response
        setTimeout(() => {
          const botMessage = document.createElement('div');
          botMessage.className = 'mb-4';
          botMessage.innerHTML = `
            <div class="inline-block bg-gray-200 rounded-lg py-2 px-4 max-w-[70%]">
              Thanks for your message! This is a demo response.
            </div>
          `;
          chatMessages.appendChild(botMessage);
          chatMessages.scrollTop = chatMessages.scrollHeight;
        }, 1000);

        // Clear input
        chatInput.value = '';
        chatMessages.scrollTop = chatMessages.scrollHeight;
      }
    }

    // Send message on button click
    sendMessage.addEventListener('click', sendChatMessage);

    // Send message on Enter key
    chatInput.addEventListener('keypress', (e) => {
      if (e.key === 'Enter' && !e.shiftKey) {
        e.preventDefault();
        sendChatMessage();
      }
    });

    // Initialize with a welcome message
    window.addEventListener('load', () => {
      const welcomeMessage = document.createElement('div');
      welcomeMessage.className = 'mb-4';
      welcomeMessage.innerHTML = `
        <div class="inline-block bg-gray-200 rounded-lg py-2 px-4 max-w-[70%]">
          Hello! How can I help you today?
        </div>
      `;
      chatMessages.appendChild(welcomeMessage);
      chatMessages.scrollTop = chatMessages.scrollHeight;
    });
  </script>

  <!-- Botpress Chatbot Embed (Optional) -->
  <script src="https://cdn.botpress.cloud/webchat/v2.4/inject.js"></script>
  <script>
    window.botpressWebChat.init({
      configUrl: "https://files.bpcontent.cloud/2025/05/18/23/20250518234039-P61UVXMH.json",
      hostUrl: "https://cdn.botpress.cloud/webchat/v2.4",
      messagingUrl: "https://messaging.botpress.cloud",
      clientId: "P61UVXMH",
      theme: "prism",
      themeColor: "#2563eb"
    });
  </script>
</body>
</html>

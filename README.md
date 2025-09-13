<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NLP Engineer Profile - [Yousef Elgohary]</title>
  <!-- React and ReactDOM from CDN -->
  <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <!-- Babel for JSX -->
  <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: #e0e0e0;
    }
  </style>
</head>
<body>
  <div id="root"></div>

  <script type="text/babel">
    const ProfileCard = () => {
      return (
        <div className="min-h-screen flex items-center justify-center">
          <div className="bg-white bg-opacity-10 backdrop-blur-md p-6 rounded-lg shadow-lg w-full max-w-md transform transition duration-500 hover:scale-105">
            <div className="text-center">
              <div className="w-32 h-32 mx-auto mb-4 rounded-full bg-gradient-to-r from-blue-400 to-purple-500 animate-pulse">
                {/* Placeholder for avatar - replace with image if generated */}
              </div>
              <h1 className="text-3xl font-bold text-white mb-2 animate-fade-in">Your Name</h1>
              <p className="text-lg text-gray-200 mb-4">NLP Engineer</p>
            </div>
            <div className="space-y-4">
              <div className="p-4 bg-gray-800 bg-opacity-70 rounded-lg animate-slide-up">
                <h2 className="text-xl font-semibold text-white">About Me</h2>
                <p className="mt-2 text-gray-300">
                  Passionate NLP Engineer specializing in building AI models for text analysis, sentiment detection, and language generation using tools like TensorFlow, PyTorch, and Hugging Face Transformers.
                </p>
              </div>
              <div className="p-4 bg-gray-800 bg-opacity-70 rounded-lg animate-slide-up delay-200">
                <h2 className="text-xl font-semibold text-white">Skills</h2>
                <ul className="mt-2 text-gray-300 list-disc list-inside">
                  <li>Python, NLP Libraries (NLTK, SpaCy)</li>
                  <li>Machine Learning (Scikit-learn, TensorFlow)</li>
                  <li>Deep Learning (LSTM, BERT)</li>
                  <li>API Development (FastAPI)</li>
                </ul>
              </div>
              <div className="p-4 bg-gray-800 bg-opacity-70 rounded-lg animate-slide-up delay-400">
                <h2 className="text-xl font-semibold text-white">Projects</h2>
                <p className="mt-2 text-gray-300">
                  - Text Sentiment Analyzer (GitHub: your-repo)
                  - Chatbot with BERT (GitHub: your-repo)
                </p>
              </div>
              <a href="https://github.com/yourusername" target="_blank" rel="noopener noreferrer" className="block text-center mt-4 text-white bg-blue-600 hover:bg-blue-700 py-2 rounded-lg transition duration-300 animate-bounce">
                Visit My GitHub
              </a>
            </div>
          </div>
        </div>
      );
    };

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<ProfileCard />);
  </script>

  <script>
    // CSS Animations
    const styleSheet = document.styleSheets[0];
    styleSheet.insertRule(`
      @keyframes fade-in {
        from { opacity: 0; }
        to { opacity: 1; }
      }
    `, styleSheet.cssRules.length);
    styleSheet.insertRule(`
      @keyframes slide-up {
        from { transform: translateY(20px); opacity: 0; }
        to { transform: translateY(0); opacity: 1; }
      }
    `, styleSheet.cssRules.length);
    styleSheet.insertRule(`
      @keyframes bounce {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-10px); }
      }
    `, styleSheet.cssRules.length);

    document.querySelectorAll('.animate-fade-in').forEach(el => {
      el.style.animation = 'fade-in 1s ease-in';
    });
    document.querySelectorAll('.animate-slide-up').forEach((el, index) => {
      el.style.animation = `slide-up 1s ease-out ${index * 0.2}s forwards`;
    });
    document.querySelectorAll('.animate-bounce').forEach(el => {
      el.style.animation = 'bounce 2s infinite';
    });
  </script>
</body>
</html>

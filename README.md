Step 1: Create Counter.jsx Component

📁 src/Counter.jsx

import { useEffect, useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    if (count !== 0 && count % 3 === 0) {
      alert(`The current number ${count} is divisible by 3`);
    }
  }, [count]); // runs ONLY when count changes

  return (
    <div>
      <h2>Counter: {count}</h2>
      <button onClick={() => setCount(count + 1)}>
        Increment
      </button>
    </div>
  );
}

export default Counter;

✅ Step 2: Import & Render in App.jsx

📁 src/App.jsx

import Counter from "./Counter";

function App() {
  return (
    <div>
      <Counter />
    </div>
  );
}

export default App;

✅ Step 3: Run the App
npm run dev

✔ Behaviour Check

Click button → count increases

When count = 3, 6, 9...

Alert shows:

The current number 3 is divisible by 3

✅ Step 4: Push to GitHub
git init
git add .
git commit -m "Counter app with useEffect dependency alert"
git branch -M main
git remote add origin <YOUR_GITHUB_REPO_URL>
git push -u origin main

📤 Submission

✅ Submit the GitHub Repository Root Folder Link

Example:

https://github.com/your-username/counter-useeffect-alert

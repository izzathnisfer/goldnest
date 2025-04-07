# GoldNest - Gold-Based Micro-Investment Platform (Devthon 2.0 Submission)

[![GoldNest Logo](https://via.placeholder.com/300x150.png?text=GoldNest+Logo)](https://www.goldnest.pages.dev)
<!-- Replace placeholder with your actual logo URL if you have one -->

**Code Mavericks** | Devthon 2.0 Final Round Submission

---

**Live Demo:** **[https://www.goldnest.pages.dev](https://www.goldnest.pages.dev)**

**GitHub Repository:** **[Your GitHub Repo Link]** <!-- <<< REPLACE THIS! -->

---

## 🚀 Project Overview

GoldNest is a web application designed as a proof-of-concept for a gold-based micro-investment platform tailored for the Sri Lankan market. It aims to provide an accessible and user-friendly way for individuals to invest in digital gold, starting with small amounts (e.g., Rs. 100), offering a potential hedge against inflation and a modern alternative to traditional savings.

This project was developed by **Team Code Mavericks** for the **Devthon 2.0** competition, progressing from an initial pool of 700 teams to the final 20 for the web implementation round.

## 🎯 Problem Statement

The Sri Lankan Rupee (LKR) faces significant inflationary pressure, diminishing the value of traditional savings held in banks that offer low-interest rates. While alternative investments exist, many (like real estate or stocks) have high entry barriers or perceived risks, leaving many Sri Lankans without accessible means to preserve and grow their wealth effectively. Gold, a historically stable asset, is often inaccessible for micro-savings due to minimum purchase requirements.

## ✨ Proposed Solution & Vision

Our original proposal envisioned GoldNest as an innovative platform leveraging **Blockchain** (for transparency and tokenized ownership) and **AI** (for investment insights) to make gold investment secure, transparent, and rewarding. Key proposed features included automated savings, peer-to-peer trading, physical redemption, and gamification.

**Due to the time constraints of the Devthon 2.0 implementation round, we focused on building a functional demonstration of the core user experience using the MERN stack.** This allowed us to deliver a working prototype showcasing the key features from our UI/UX design submission. The integration of blockchain and AI remains a key part of the future vision for GoldNest.

## ✅ Implemented Features (Functional Demo)

*   **User Authentication:**
    *   Secure User Signup & Login (Modal-based).
    *   Forgot Password & Reset Password functionality.
    *   JWT-based session management.
    *   Password hashing (bcrypt).
*   **Protected Dashboard:** Accessible only to logged-in users, displaying key account information.
*   **Dynamic Gold Balance:** Simulation of gold ownership (grams), updated via investments.
*   **Investment Module:**
    *   Page for making simulated gold investments (minimum Rs. 100).
    *   Updates user's gold balance in the backend database.
    *   Option to automatically create a recurring 'Automatic Payment' setting upon investment.
*   **Wallet Page:**
    *   Displays current gold balance and its estimated LKR value (based on a simulated price).
    *   Fetches and displays **dynamic transaction history** from the backend.
    *   Simulates progress towards redeeming physical gold coins based on balance.
    *   Displays simulated redemption history.
*   **Gamification Display:**
    *   Structured display of defined badges and active challenges.
    *   Fetches user's *earned* badge IDs (though awarding logic is future scope).
    *   Simulates challenge progress display based on user data.
*   **Settings Page:**
    *   Tabbed interface (General, Payment, Security, Account, Help).
    *   **Dynamic General Settings:** Edit Name, Phone, Address, City (updates profile).
    *   **Dynamic Payment Settings:** Full CRUD (Create, Read, Update, Delete) functionality for Automatic Payment schedules.
    *   **Dynamic Security Settings:** Change Password functionality.
    *   **Simulated Security:** Visual toggles for 2FA/PIN (functionality not implemented).
    *   **Simulated Account:** Display/buttons for account deletion (backend logic not implemented).
*   **Responsive UI:** Based on the Figma design submitted in the previous round (continuous polishing).

## 🛠️ Technology Stack (Actual Implementation)

*   **Frontend:** Next.js (React Framework), JavaScript, CSS (using `globals.css` based on teammate's `styles.css`), Axios (for API calls)
*   **Backend:** Node.js, Express.js
*   **Database:** MongoDB Atlas (Cloud NoSQL Database), Mongoose (ODM)
*   **Authentication:** JSON Web Tokens (JWT), bcrypt.js (Password Hashing)
*   **Deployment:** Vercel / Cloudflare Pages (as indicated by demo link)
*   **Version Control:** Git, GitHub

## 📸 Screenshots

*Include high-quality screenshots or GIFs of your application here. Show key pages like:*

*   *Login Modal*
*   *Signup Page*
*   *Dashboard Overview*
*   *Invest Page*
*   *Wallet Page (showing transactions/progress)*
*   *Settings Page (e.g., Auto Payments section)*

`![Login Modal](link-to-your-screenshot-1.png)`
`![Dashboard](link-to-your-screenshot-2.png)`
`![Wallet](link-to-your-screenshot-3.png)`
`![Settings](link-to-your-screenshot-4.png)`
<!-- Add more as needed -->

## ⚙️ Getting Started / Local Setup

Follow these instructions to set up and run the project locally.

**Prerequisites:**

*   Node.js (v16 or later recommended)
*   npm or yarn
*   Git
*   MongoDB Atlas Account (free tier is sufficient)

**Setup:**

1.  **Clone the repository:**
    ```bash
    git clone [Your GitHub Repo Link]
    cd [your-repo-folder-name]
    ```

2.  **Backend Setup:**
    ```bash
    cd backend
    npm install
    ```
    *   Create a `.env` file in the `/backend` directory.
    *   Add the following environment variables:
        ```dotenv
        NODE_ENV=development
        PORT=5001
        MONGO_URI=[Your MongoDB Atlas Connection String] # Replace <password> with your DB user password!
        JWT_SECRET=[Your Secure Random String for JWT] # e.g., YourVerySecretKeyForTokens123
        ```
    *   Run the backend server:
        ```bash
        npm run dev
        ```
    *   The backend should now be running on `http://localhost:5001`.

3.  **Frontend Setup:**
    ```bash
    cd ../frontend
    npm install
    ```
    *   Create a `.env.local` file in the `/frontend` directory.
    *   Add the following environment variable:
        ```dotenv
        NEXT_PUBLIC_BACKEND_URL=http://localhost:5001 # Point to your local backend
        ```
    *   Run the frontend development server:
        ```bash
        npm run dev
        ```
    *   Open your browser and navigate to `http://localhost:3000`.

## 🔮 Future Enhancements

While this submission represents a functional proof-of-concept based on the UI design, the following key features from the original proposal are identified as future scope:

*   **Blockchain Integration:** Implementing tokenization of gold assets on a suitable blockchain (e.g., Polygon) for enhanced transparency and potentially enabling P2P transfers.
*   **AI-Driven Insights:** Integrating AI/ML models to provide users with personalized investment suggestions, market trend analysis, and risk assessment.
*   **Real Payment Gateway Integration:** Connecting with PayHere, FriMi, etc., for actual LKR transactions.
*   **Physical Gold Redemption Logic:** Implementing the backend workflow and partnerships required for users to redeem their digital gold balance for physical coins.
*   **Dynamic Gamification Logic:** Implementing backend logic to automatically track user progress towards challenges and award badges based on defined criteria.
*   **Full Security Implementation:** Enabling functional 2FA and PIN verification.
*   **Peer-to-Peer Features:** Building modules for users to trade or lend gold assets within the platform.

## 🧑‍💻 Team: Code Mavericks

*   **M J S Ahamed (Sabith)** - Team Leader, Frontend Development
*   **Rahim Iqbal** - Frontend Development
*   **Izzath Nisfer** - Backend Development

## 🙏 Acknowledgements

We thank the organizers of **Devthon 2.0** and **SLTC** for this challenging and rewarding competition opportunity.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

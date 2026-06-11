/* Reset default browser spacing */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Deep dark background for the entire page */
body {
    background-color: #020617;
    color: #ffffff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

/* Running Ticker Bar Styling */
.ticker-wrap {
    width: 100%;
    background: linear-gradient(90deg, #10b981, #06b6d4, #6366f1);
    color: #020617;
    font-weight: bold;
    padding: 10px;
    overflow: hidden;
    position: sticky;
    top: 0;
    z-index: 100;
}

.ticker-text {
    display: inline-block;
    white-space: nowrap;
    padding-left: 100%;
    animation: marquee 25s linear infinite;
}

@keyframes marquee {
    0% { transform: translate3d(0, 0, 0); }
    100% { transform: translate3d(-100%, 0, 0); }
}

/* Main Layout Grid */
.container {
    max-width: 1200px;
    margin: 30px auto;
    padding: 0 20px;
    width: 100%;
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 30px;
}

/* Responsive adjustment for mobile screens */
@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }
}

/* Content Cards */
.card {
    background-color: #0f172a;
    border: 2px solid #1e293b;
    border-radius: 16px;
    padding: 24px;
    margin-bottom: 24px;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3);
}

.card-premium {
    border-color: rgba(16, 185, 129, 0.3);
    background: linear-gradient(135deg, #0f172a 0%, #030712 100%);
}

/* Typography & Accent Colors */
h1, h2, h3 {
    margin-bottom: 15px;
    font-weight: 800;
}

.text-gradient {
    background: linear-gradient(90deg, #34d399, #22d3ee);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.text-emerald { color: #10b981; }
.text-cyan { color: #22d3ee; }
.text-yellow { color: #f59e0b; }

/* Input fields */
.input-field {
    width: 100%;
    background-color: #1e293b;
    border: 2px solid #334155;
    border-radius: 8px;
    padding: 12px;
    color: white;
    font-size: 16px;
    margin-top: 8px;
    outline: none;
}

.input-field:focus {
    border-color: #10b981;
}

/* Buttons */
.btn-submit {
    width: 100%;
    background: linear-gradient(90deg, #10b981, #06b6d4);
    color: #020617;
    font-weight: bold;
    padding: 14px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-size: 16px;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: opacity 0.2s;
}

.btn-submit:hover {
    opacity: 0.9;
}

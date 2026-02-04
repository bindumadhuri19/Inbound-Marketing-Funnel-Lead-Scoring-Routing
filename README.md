<!DOCTYPE html>
<html>
<body>

    <h1>Inbound Marketing Funnel – Lead Scoring & Routing</h1>

    <section>
        <h2>📌 Project Overview</h2>
        <p>This project is an automated lead-management system built in <strong>Zapier</strong>. It is designed to bridge the gap between marketing and sales by automatically identifying, scoring, and routing leads based on their business value.</p>
        
        <h3>🚀 Key Features:</h3>
        <ul>
            <li><strong>Real-Time Capture:</strong> Instantly pulls data from Google Forms.</li>
            <li><strong>Intelligent Scoring:</strong> Uses a custom Lookup Table to weight leads by job role.</li>
            <li><strong>Automated Enrichment:</strong> Uses Apollo to find prospect details for high-value leads.</li>
            <li><strong>Dynamic Routing:</strong> Sends "Hot Leads" to Pipedrive CRM and "Nurture Leads" to Google Sheets.</li>
        </ul>
    </section>

    <hr>

    <section>
        <h2>🛠️ The Workflow Architecture</h2>
        
        <h3>1. Trigger: Google Forms</h3>
        <ul>
            <li><strong>Action:</strong> New Form Response.</li>
            <li><strong>Implementation:</strong> Captures the lead's name, email, and job role to kick off the automation instantly.</li>
        </ul>

        <h3>2. Logic: Formatter by Zapier (Utilities)</h3>
        <ul>
            <li><strong>Action:</strong> Lookup Table.</li>
            <li><strong>Implementation:</strong> I implemented this as the "brain" of the flow. It assigns numeric values to roles (e.g., Founder = 50, Individual = 5).</li>
        </ul>

        <h3>3. Branching: Paths</h3>
        <ul>
            <li><strong>Action:</strong> Conditional Logic.</li>
            <li><strong>Implementation:</strong> Leads with a score over 40 are routed to the Sales Path, while everyone else is sent to the Nurture Path.</li>
        </ul>

        <h3>4. Path A: Sales Execution (High-Value)</h3>
        <ul>
            <li><strong>Apollo integration:</strong> Automatically finds the prospect's LinkedIn or persona data.</li>
            <li><strong>Pipedrive integration:</strong> Creates a new Lead and Deal in the CRM for immediate sales follow-up.</li>
            <li><strong>Gmail Notification:</strong> Sends an instant alert to the sales team.</li>
        </ul>

        <h3>5. Path B: Marketing Nurture (Low-Value)</h3>
        <ul>
            <li><strong>Google Sheets integration:</strong> Maps lead data into a structured archival system.</li>
            <li><strong>Data Integrity:</strong> I implemented specific headers (Name, Email, Score) to ensure a clean database for future campaigns.</li>
        </ul>
    </section>

    

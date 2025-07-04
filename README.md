# CHROME-EXTENSION-FOR-TIME-TRACKING-AND-PRODUCTIVITY-ANALYTICS

"COMPANY": CODTECH IT SOLUTIONS

"NAME": BADA SAMYADEVI

"INTERN ID": CT04DG512

"DOMAIN": FULL STACK WEB DEVELOPMENT

"DURATION": 4 WEEKS

"MENTOR": NEELA SANTOSH

DESCRIPTION:

* This project is a robust Chrome Extension meticulously designed to empower users with insightful TRACKER AND PRODUCTIVITY analytics of their web browsing habits. It operates seamlessly in the background, collecting valuable data on time spent across various websites, which is then presented through intuitive visual dashboards. The extension aims to foster greater awareness and control over digital consumption, helping users identify and optimize their online efficiency.

* At its core, the extension relies on a well-defined structure orchestrated by the manifest.json file. This crucial configuration file acts as the blueprint, declaring the extension's identity ("Web Activity Logger"), its version, and specifying all necessary permissions, such as tabs (to monitor browser activity), activeTab (to identify the currently focused tab), storage (for data persistence), and alarms (for periodic operations, though the latest background script focuses on event-driven tracking). It also meticulously links all other components, including the background service worker, the popup interface, and the dedicated options and dashboard pages, ensuring Chrome correctly loads and operates the extension.

* The engine of the tracking mechanism resides within background.js. This script functions as a persistent tracker, running quietly in the browser's background as a service worker. It diligently monitors user interaction by listening to browser events like chrome.tabs.onActivated (when a user switches tabs), chrome.tabs.onUpdated (when a URL changes within an active tab), and chrome.windows.onFocusChanged (when the Chrome browser gains or loses focus). Upon these events, it calculates the duration a user spends on a specific website domain and saves this raw time data directly into chrome.storage.local. This ensures that tracking data is preserved even if the browser is closed and reopened, providing a continuous log of web activity.

* For quick glances at real-time activity, the extension provides a compact user interface via popup.html and popup.js. When the user clicks the extension icon in the Chrome toolbar, popup.html renders a minimalistic display. The accompanying popup.js script then communicates with background.js to retrieve the latest tracked data. It processes this information to present a concise overview of visited websites and the total time spent on each, offering immediate feedback on current browsing patterns.

* The true analytical power of the extension is unleashed through the dashboard.html and dashboard.js components. dashboard.html serves as a dedicated analytics page, featuring a <canvas> element that acts as the drawing board for data visualizations. The sophisticated logic within dashboard.js takes center stage here. It fetches the raw time-tracking data from storage and performs crucial productivity analytics. This includes categorizing websites as "productive," "unproductive," or "neutral" based on predefined lists (currently hardcoded within dashboard.js itself, though designed for future user configurability via an options page). The processed data is then fed into the integrated chart.js library.

* chart.js is a powerful third-party JavaScript library that enables the dynamic creation of rich, interactive charts. dashboard.js leverages chart.js to generate compelling visual reports, such as a bar chart illustrating time spent on individual websites and a pie chart providing an overall breakdown of productive, unproductive, and neutral time. These visualizations, coupled with a textual summary of total time and productivity percentages, offer users a clear, digestible overview of their online behavior.

* In summary, this Chrome Extension provides a comprehensive solution for web activity tracking and productivity analytics. By combining background data collection, user-friendly pop-up summaries, and detailed visual reports powered by Chart.js, it empowers users to gain deeper insights into their digital habits and make informed decisions to enhance their online productivity.

 

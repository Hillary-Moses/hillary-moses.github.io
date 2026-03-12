# hillary-moses.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>📦 Farm Haulage Tracker - A, B, C, D, E, F</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Segoe UI Emoji', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            overflow: hidden;
            padding: 25px;
        }
        
        /* Header */
        .header {
            text-align: center;
            padding: 20px 0 30px;
            background: linear-gradient(to right, #4CAF50, #2E7D32);
            margin: -25px -25px 25px;
            color: white;
            border-bottom: 5px solid #1B5E20;
        }
        
        h1 {
            font-size: 28px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        h1 i {
            font-size: 32px;
        }
        
        .subtitle {
            font-size: 16px;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        /* Navigation */
        .nav-tabs {
            display: flex;
            background: #f1f8e9;
            border-radius: 12px;
            margin-bottom: 25px;
            overflow: hidden;
            border: 2px solid #c5e1a5;
        }
        
        .tab {
            flex: 1;
            padding: 15px;
            text-align: center;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            border-bottom: 3px solid transparent;
        }
        
        .tab.active {
            background: #4CAF50;
            color: white;
            border-bottom: 3px solid #1B5E20;
        }
        
        .tab i {
            margin-right: 8px;
        }
        
        /* Tab Content */
        .tab-content {
            display: none;
            animation: fadeIn 0.5s;
        }
        
        .tab-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Card Styling */
        .card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            border-left: 6px solid #4CAF50;
        }
        
        .card h2 {
            color: #2E7D32;
            margin-bottom: 20px;
            font-size: 22px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 2px solid #e8f5e9;
            padding-bottom: 10px;
        }
        
        /* Staff Selector */
        .staff-selector {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            margin: 20px 0;
        }
        
        .staff-btn {
            padding: 18px 10px;
            border: 3px solid #ddd;
            border-radius: 12px;
            background: white;
            font-size: 20px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }
        
        .staff-btn i {
            font-size: 24px;
        }
        
        .staff-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0,0,0,0.1);
        }
        
        .staff-btn.selected {
            background: #4CAF50;
            color: white;
            border-color: #2E7D32;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(76, 175, 80, 0.3);
        }
        
        .staff-A { color: #FF5722; border-color: #FF5722; }
        .staff-B { color: #2196F3; border-color: #2196F3; }
        .staff-C { color: #4CAF50; border-color: #4CAF50; }
        .staff-D { color: #FFC107; border-color: #FFC107; }
        .staff-E { color: #9C27B0; border-color: #9C27B0; }
        .staff-F { color: #795548; border-color: #795548; }
        
        .staff-btn.selected.staff-A { background: #FF5722; }
        .staff-btn.selected.staff-B { background: #2196F3; }
        .staff-btn.selected.staff-C { background: #4CAF50; }
        .staff-btn.selected.staff-D { background: #FFC107; }
        .staff-btn.selected.staff-E { background: #9C27B0; }
        .staff-btn.selected.staff-F { background: #795548; }
        
        /* Form Elements */
        .input-group {
            margin: 20px 0;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            color: #555;
            font-weight: 600;
            font-size: 16px;
        }
        
        input, select {
            width: 100%;
            padding: 15px;
            border: 2px solid #c8e6c9;
            border-radius: 10px;
            font-size: 16px;
            transition: border 0.3s;
        }
        
        input:focus, select:focus {
            outline: none;
            border-color: #4CAF50;
            box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.2);
        }
        
        /* Buttons */
        .btn-group {
            display: flex;
            gap: 15px;
            margin-top: 25px;
        }
        
        .btn {
            flex: 1;
            padding: 18px;
            border: none;
            border-radius: 12px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 7px 15px rgba(0,0,0,0.15);
        }
        
        .btn:active {
            transform: translateY(-1px);
        }
        
        .btn-primary {
            background: linear-gradient(to right, #2196F3, #1976D2);
            color: white;
        }
        
        .btn-success {
            background: linear-gradient(to right, #4CAF50, #2E7D32);
            color: white;
        }
        
        .btn-warning {
            background: linear-gradient(to right, #FF9800, #EF6C00);
            color: white;
        }
        
        .btn-danger {
            background: linear-gradient(to right, #F44336, #C62828);
            color: white;
        }
        
        .btn-secondary {
            background: linear-gradient(to right, #757575, #424242);
            color: white;
        }
        
        /* Stats Display */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }
        
        .stat-box {
            background: #f1f8e9;
            padding: 20px;
            border-radius: 12px;
            text-align: center;
            border-top: 5px solid #4CAF50;
            transition: transform 0.3s;
        }
        
        .stat-box:hover {
            transform: translateY(-5px);
        }
        
        .stat-value {
            font-size: 32px;
            font-weight: bold;
            color: #2E7D32;
            margin: 10px 0;
        }
        
        .stat-label {
            font-size: 14px;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .stat-details {
            font-size: 13px;
            color: #4CAF50;
            margin-top: 8px;
            font-weight: 600;
        }
        
        /* Activity Log */
        .activity-log {
            max-height: 400px;
            overflow-y: auto;
            margin-top: 15px;
        }
        
        .log-entry {
            padding: 15px;
            border-bottom: 1px solid #e0e0e0;
            display: flex;
            align-items: center;
            gap: 15px;
            animation: slideIn 0.5s;
        }
        
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-20px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .log-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: white;
            flex-shrink: 0;
        }
        
        .log-content {
            flex: 1;
        }
        
        .log-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .log-staff {
            font-weight: bold;
            font-size: 18px;
        }
        
        .log-time {
            color: #666;
            font-size: 14px;
        }
        
        .log-details {
            color: #555;
            font-size: 15px;
        }
        
        .log-packages {
            background: #e8f5e9;
            color: #2E7D32;
            padding: 3px 10px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 14px;
        }
        
        /* SMS Instructions */
        .sms-card {
            background: #e3f2fd;
            border-left-color: #2196F3;
        }
        
        .sms-example {
            background: white;
            padding: 15px;
            border-radius: 10px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            border-left: 4px solid #2196F3;
        }
        
        .sms-example h4 {
            color: #2196F3;
            margin-bottom: 10px;
        }
        
        /* Settings */
        .settings-group {
            margin-bottom: 25px;
        }
        
        .setting-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px;
            background: #f5f5f5;
            border-radius: 10px;
            margin-bottom: 10px;
        }
        
        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 30px;
        }
        
        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: .4s;
            border-radius: 34px;
        }
        
        .slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }
        
        input:checked + .slider {
            background-color: #4CAF50;
        }
        
        input:checked + .slider:before {
            transform: translateX(30px);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding-top: 20px;
            margin-top: 20px;
            border-top: 1px solid #e0e0e0;
            color: #666;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 600px) {
            .staff-selector {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .btn-group {
                flex-direction: column;
            }
            
            .container {
                padding: 15px;
            }
            
            .header {
                padding: 15px 0 20px;
            }
            
            h1 {
                font-size: 24px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1><i class="fas fa-truck-loading"></i> Farm Haulage Tracker</h1>
            <p class="subtitle">Tracking Staff: A, B, C, D, E, F</p>
            <p id="currentDate" style="font-size: 14px; opacity: 0.9;"></p>
        </div>
        
        <!-- Navigation Tabs -->
        <div class="nav-tabs">
            <div class="tab active" onclick="switchTab('log')">
                <i class="fas fa-clipboard-list"></i> Log Trip
            </div>
            <div class="tab" onclick="switchTab('stats')">
                <i class="fas fa-chart-bar"></i> Stats
            </div>
            <div class="tab" onclick="switchTab('activity')">
                <i class="fas fa-history"></i> Activity
            </div>
            <div class="tab" onclick="switchTab('sms')">
                <i class="fas fa-sms"></i> SMS Mode
            </div>
            <div class="tab" onclick="switchTab('settings')">
                <i class="fas fa-cog"></i> Settings
            </div>
        </div>
        
        <!-- Tab 1: Log Trip -->
        <div id="log-tab" class="tab-content active">
            <div class="card">
                <h2><i class="fas fa-plus-circle"></i> Log New Trip</h2>
                
                <div class="input-group">
                    <label><i class="fas fa-user"></i> Select Staff Member</label>
                    <div class="staff-selector">
                        <button class="staff-btn staff-A" data-staff="A">
                            <i class="fas fa-user"></i>
                            <span>Staff A</span>
                        </button>
                        <button class="staff-btn staff-B" data-staff="B">
                            <i class="fas fa-user"></i>
                            <span>Staff B</span>
                        </button>
                        <button class="staff-btn staff-C" data-staff="C">
                            <i class="fas fa-user"></i>
                            <span>Staff C</span>
                        </button>
                        <button class="staff-btn staff-D" data-staff="D">
                            <i class="fas fa-user"></i>
                            <span>Staff D</span>
                        </button>
                        <button class="staff-btn staff-E" data-staff="E">
                            <i class="fas fa-user"></i>
                            <span>Staff E</span>
                        </button>
                        <button class="staff-btn staff-F" data-staff="F">
                            <i class="fas fa-user"></i>
                            <span>Staff F</span>
                        </button>
                    </div>
                </div>
                
                <div class="input-group">
                    <label><i class="fas fa-hashtag"></i> Trip Number Today</label>
                    <select id="tripNumber">
                        <option value="1">Trip 1</option>
                        <option value="2">Trip 2</option>
                        <option value="3">Trip 3</option>
                        <option value="4">Trip 4</option>
                        <option value="5">Trip 5</option>
                        <option value="6">Trip 6</option>
                        <option value="7">Trip 7</option>
                        <option value="8">Trip 8</option>
                        <option value="9">Trip 9</option>
                        <option value="10">Trip 10</option>
                        <option value="11">Trip 11</option>
                        <option value="12">Trip 12</option>
                        <option value="13">Trip 13</option>
                        <option value="14">Trip 14</option>
                        <option value="15">Trip 15</option>
                    </select>
                </div>
                
                <div class="input-group">
                    <label><i class="fas fa-box"></i> Number of Packages</label>
                    <input type="number" id="packages" min="1" max="100" value="1">
                </div>
                
                <div class="input-group">
                    <label><i class="fas fa-map-marker-alt"></i> Location Notes (Optional)</label>
                    <input type="text" id="locationNotes" placeholder="E.g., From North Field to Main Road">
                </div>
                
                <div class="btn-group">
                    <button class="btn btn-success" onclick="logTrip()">
                        <i class="fas fa-check-circle"></i> Log Trip
                    </button>
                    <button class="btn btn-secondary" onclick="resetForm()">
                        <i class="fas fa-redo"></i> Reset
                    </button>
                </div>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-info-circle"></i> Quick Instructions</h2>
                <p>1. Select the staff member who completed the trip</p>
                <p>2. Enter the trip number (1st, 2nd, 3rd trip today)</p>
                <p>3. Enter number of packages moved</p>
                <p>4. Click "Log Trip" to record</p>
                <p style="margin-top: 15px; color: #4CAF50; font-weight: 600;">
                    <i class="fas fa-sync-alt"></i> Data saves automatically to your phone
                </p>
            </div>
        </div>
        
        <!-- Tab 2: Statistics -->
        <div id="stats-tab" class="tab-content">
            <div class="card">
                <h2><i class="fas fa-chart-pie"></i> Today's Summary</h2>
                <div id="statsContainer" class="stats-grid">
                    <!-- Stats will load here -->
                </div>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-trophy"></i> Performance Leaderboard</h2>
                <div id="leaderboardContainer">
                    <!-- Leaderboard will load here -->
                </div>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-calendar-alt"></i> Weekly Overview</h2>
                <div id="weeklyStats">
                    <p>Weekly data will appear here after multiple days of tracking</p>
                </div>
            </div>
        </div>
        
        <!-- Tab 3: Activity Log -->
        <div id="activity-tab" class="tab-content">
            <div class="card">
                <h2><i class="fas fa-list-alt"></i> Recent Activity</h2>
                <div class="btn-group" style="margin-top: 0; margin-bottom: 20px;">
                    <button class="btn btn-primary" onclick="filterActivity('all')">
                        <i class="fas fa-list"></i> All
                    </button>
                    <button class="btn btn-secondary" onclick="filterActivity('today')">
                        <i class="fas fa-sun"></i> Today
                    </button>
                    <button class="btn btn-warning" onclick="clearAllData()">
                        <i class="fas fa-trash"></i> Clear All
                    </button>
                </div>
                
                <div id="activityLog" class="activity-log">
                    <!-- Activity logs will appear here -->
                </div>
            </div>
        </div>
        
        <!-- Tab 4: SMS Mode -->
        <div id="sms-tab" class="tab-content">
            <div class="card">
                <h2><i class="fas fa-mobile-alt"></i> SMS/WhatsApp Tracking</h2>
                <p>Use this method if staff have basic phones. They can send SMS/WhatsApp messages in this format:</p>
                
                <div class="sms-example">
                    <h4><i class="fas fa-sms"></i> Format:</h4>
                    <p><strong>[STAFF] [TRIP#] [P/C] [PACKAGES#]</strong></p>
                    <p style="margin-top: 10px; font-size: 13px;">
                        P = Starting trip (Pickup)<br>
                        C = Completed trip
                    </p>
                </div>
                
                <div class="sms-example">
                    <h4><i class="fas fa-comment-dots"></i> Examples:</h4>
                    <p><code>A 1 P</code> - Staff A starting Trip 1</p>
                    <p><code>A 1 C 12</code> - Staff A completed Trip 1 with 12 packages</p>
                    <p><code>B 2 P</code> - Staff B starting Trip 2</p>
                    <p><code>B 2 C 8</code> - Staff B completed Trip 2 with 8 packages</p>
                </div>
                
                <div class="input-group">
                    <label><i class="fas fa-phone"></i> Enter SMS to Simulate</label>
                    <input type="text" id="smsInput" placeholder="Enter SMS like: A 1 C 12">
                </div>
                
                <button class="btn btn-primary" onclick="processSMS()" style="width: 100%;">
                    <i class="fas fa-paper-plane"></i> Process SMS
                </button>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-qrcode"></i> QR Code System</h2>
                <p>Print QR codes for each staff to scan and log trips quickly:</p>
                <div id="qrcodes" style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 15px; margin-top: 15px;">
                    <!-- QR codes will be generated here -->
                </div>
            </div>
        </div>
        
        <!-- Tab 5: Settings -->
        <div id="settings-tab" class="tab-content">
            <div class="card">
                <h2><i class="fas fa-cogs"></i> Application Settings</h2>
                
                <div class="settings-group">
                    <h3 style="margin-bottom: 15px; color: #555;">Security Settings</h3>
                    
                    <div class="setting-item">
                        <div>
                            <strong><i class="fas fa-lock"></i> PIN Protection</strong>
                            <p style="font-size: 14px; color: #666; margin-top: 5px;">Require PIN for staff login</p>
                        </div>
                        <label class="toggle-switch">
                            <input type="checkbox" id="pinProtection">
                            <span class="slider"></span>
                        </label>
                    </div>
                    
                    <div class="setting-item">
                        <div>
                            <strong><i class="fas fa-bell"></i> Daily Reset Notification</strong>
                            <p style="font-size: 14px; color: #666; margin-top: 5px;">Remind to reset data daily</p>
                        </div>
                        <label class="toggle-switch">
                            <input type="checkbox" id="dailyReset" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                </div>
                
                <div class="settings-group">
                    <h3 style="margin-bottom: 15px; color: #555;">Data Management</h3>
                    
                    <button class="btn btn-primary" onclick="exportData()" style="width: 100%; margin-bottom: 10px;">
                        <i class="fas fa-download"></i> Export All Data
                    </button>
                    
                    <button class="btn btn-warning" onclick="resetDailyData()" style="width: 100%; margin-bottom: 10px;">
                        <i class="fas fa-calendar-day"></i> Reset Today's Data
                    </button>
                    
                    <button class="btn btn-danger" onclick="clearAllData()" style="width: 100%;">
                        <i class="fas fa-trash-alt"></i> Clear All Data
                    </button>
                </div>
                
                <div class="settings-group">
                    <h3 style="margin-bottom: 15px; color: #555;">Staff PINs</h3>
                    <div id="pinSettings">
                        <!-- PIN settings will be generated here -->
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Footer -->
        <div class="footer">
            <p><i class="fas fa-code"></i> Farm Haulage Tracker v1.0 | Staff: A, B, C, D, E, F</p>
            <p style="margin-top: 10px; font-size: 12px;">Data is stored locally on your device</p>
        </div>
    </div>

    <script>
        // Initialize data storage
        let haulageData = JSON.parse(localStorage.getItem('haulageData')) || {
            date: new Date().toISOString().split('T')[0],
            trips: [],
            staffPins: {
                'A': '1234', 'B': '2345', 'C': '3456',
                'D': '4567', 'E': '5678', 'F': '6789'
            },
            settings: {
                pinProtection: false,
                dailyReset: true
            }
        };
        
        let selectedStaff = null;
        let currentFilter = 'today';
        
        // Initialize on page load
        document.addEventListener('DOMContentLoaded', function() {
            // Set current date
            const now = new Date();
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('currentDate').textContent = now.toLocaleDateString('en-US', options);
            
            // Initialize staff buttons
            document.querySelectorAll('.staff-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('.staff-btn').forEach(b => b.classList.remove('selected'));
                    this.classList.add('selected');
                    selectedStaff = this.dataset.staff;
                    
                    // Check if PIN protection is enabled
                    if (haulageData.settings.pinProtection) {
                        const pin = prompt(`Enter PIN for Staff ${selectedStaff}:`);
                        if (pin !== haulageData.staffPins[selectedStaff]) {
                            alert('Invalid PIN!');
                            this.classList.remove('selected');
                            selectedStaff = null;
                        }
                    }
                });
            });
            
            // Load settings
            document.getElementById('pinProtection').checked = haulageData.settings.pinProtection;
            document.getElementById('dailyReset').checked = haulageData.settings.dailyReset;
            
            // Generate PIN settings UI
            generatePinSettings();
            
            // Generate QR codes
            generateQRCodes();
            
            // Check if we need to reset for new day
            checkDailyReset();
            
            // Update all displays
            updateAllDisplays();
        });
        
        // Tab switching
        function switchTab(tabName) {
            // Update active tab
            document.querySelectorAll('.tab').forEach(tab => tab.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(content => content.classList.remove('active'));
            
            event.target.closest('.tab').classList.add('active');
            document.getElementById(`${tabName}-tab`).classList.add('active');
            
            // Refresh data when switching to stats tab
            if (tabName === 'stats') {
                updateStats();
                updateLeaderboard();
            } else if (tabName === 'activity') {
                updateActivityLog();
            }
        }
        
        // Log a new trip
        function logTrip() {
            if (!selectedStaff) {
                alert('Please select a staff member first!');
                return;
            }
            
            const tripNumber = document.getElementById('tripNumber').value;
            const packages = document.getElementById('packages').value;
            const location = document.getElementById('locationNotes').value || 'Farm to Road';
            const timestamp = new Date();
            const timeString = timestamp.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
            
            if (!packages || packages < 1) {
                alert('Please enter a valid number of packages!');
                return;
            }
            
            const trip = {
                id: Date.now(),
                staff: selectedStaff,
                tripNumber: parseInt(tripNumber),
                packages: parseInt(packages),
                location: location,
                time: timeString,
                fullTime: timestamp.toISOString(),
                date: timestamp.toISOString().split('T')[0]
            };
            
            haulageData.trips.push(trip);
            saveData();
            
            // Reset form and show confirmation
            resetForm();
            showNotification(`Trip logged for Staff ${trip.staff}! ${trip.packages} packages moved.`);
            
            // Update displays
            updateAllDisplays();
            
            // Switch to activity tab to show the new log
            switchTab('activity');
        }
        
        // Process SMS input
        function processSMS() {
            const smsInput = document.getElementById('smsInput').value.trim().toUpperCase();
            if (!smsInput) {
                alert('Please enter an SMS message!');
                return;
            }
            
            // Parse SMS format: [STAFF] [TRIP#] [P/C] [PACKAGES#]
            const parts = smsInput.split(' ');
            if (parts.length < 3) {
                alert('Invalid SMS format! Use: [STAFF] [TRIP#] [P/C] [PACKAGES#]');
                return;
            }
            
            const staff = parts[0];
            const tripNumber = parts[1];
            const status = parts[2];
            const packages = parts[3] || '1';
            
            if (!['A','B','C','D','E','F'].includes(staff)) {
                alert('Invalid staff! Use A, B, C, D, E, or F');
                return;
            }
            
            if (status === 'P') {
                // Starting trip
                showNotification(`Staff ${staff} started Trip ${tripNumber}`);
            } else if (status === 'C') {
                // Completed trip - log it
                const timestamp = new Date();
                const timeString = timestamp.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
                
                const trip = {
                    id: Date.now(),
                    staff: staff,
                    tripNumber: parseInt(tripNumber),
                    packages: parseInt(packages),
                    location: 'Via SMS',
                    time: timeString,
                    fullTime: timestamp.toISOString(),
                    date: timestamp.toISOString().split('T')[0]
                };
                
                haulageData.trips.push(trip);
                saveData();
                
                showNotification(`Trip logged for Staff ${staff} via SMS! Trip ${tripNumber} with ${packages} packages.`);
                updateAllDisplays();
            } else {
                alert('Invalid status! Use P for starting or C for completed trip.');
            }
            
            // Clear input
            document.getElementById('smsInput').value = '';
        }
        
        // Reset form
        function resetForm() {
            document.querySelectorAll('.staff-btn').forEach(b => b.classList.remove('selected'));
            selectedStaff = null;
            document.getElementById('packages').value = 1;
            document.getElementById('locationNotes').value = '';
            
            // Auto-increment trip number for next entry
            const currentTripNumber = parseInt(document.getElementById('tripNumber').value);
            if (currentTripNumber < 15) {
                document.getElementById('tripNumber').value = currentTripNumber + 1;
            }
        }
        
        // Update all displays
        function updateAllDisplays() {
            updateStats();
            updateLeaderboard();
            updateActivityLog();
            generateQRCodes();
        }
        
        // Update statistics
        function updateStats() {
            const statsContainer = document.getElementById('statsContainer');
            const today = new Date().toISOString().split('T')[0];
            const todayTrips = haulageData.trips.filter(trip => trip.date === today);
            
            let statsHTML = '';
            ['A', 'B', 'C', 'D', 'E', 'F'].forEach(staff => {
                const staffTrips = todayTrips.filter(trip => trip.staff === staff);
                const totalTrips = staffTrips.length;
                const totalPackages = staffTrips.reduce((sum, trip) => sum + trip.packages, 0);
                
                statsHTML += `
                    <div class="stat-box">
                        <div class="stat-label">Staff ${staff}</div>
                        <div class="stat-value">${totalTrips}</div>
                        <div class="stat-details">
                            <i class="fas fa-box"></i> ${totalPackages} packages
                        </div>
                        <div style="font-size: 12px; color: #999; margin-top: 5px;">
                            ${totalTrips === 0 ? 'No trips today' : 'Avg: ' + Math.round(totalPackages/totalTrips) + '/trip'}
                        </div>
                    </div>
                `;
            });
            
            statsContainer.innerHTML = statsHTML;
        }
        
        // Update leaderboard
        function updateLeaderboard() {
            const leaderboardContainer = document.getElementById('leaderboardContainer');
            const today = new Date().toISOString().split('T')[0];
            const todayTrips = haulageData.trips.filter(trip => trip.date === today);
            
            // Calculate totals for each staff
            const staffTotals = {};
            ['A', 'B', 'C', 'D', 'E', 'F'].forEach(staff => {
                const staffTrips = todayTrips.filter(trip => trip.staff === staff);
                staffTotals[staff] = {
                    trips: staffTrips.length,
                    packages: staffTrips.reduce((sum, trip) => sum + trip.packages, 0)
                };
            });
            
            // Sort by number of trips (then packages)
            const sortedStaff = Object.entries(staffTotals)
                .sort((a, b) => {
                    if (b[1].trips !== a[1].trips) return b[1].trips - a[1].trips;
                    return b[1].packages - a[1].packages;
                });
            
            let leaderboardHTML = '';
            let rank = 1;
            sortedStaff.forEach(([staff, data]) => {
                if (data.trips > 0) {
                    leaderboardHTML += `
                        <div class="log-entry" style="margin-bottom: 10px; border-radius: 10px; border-left: 5px solid ${getStaffColor(staff)};">
                            <div class="log-icon" style="background: ${getStaffColor(staff)};">
                                ${rank === 1 ? '🥇' : rank === 2 ? '🥈' : rank === 3 ? '🥉' : rank}
                            </div>
                            <div class="log-content">
                                <div class="log-header">
                                    <div class="log-staff">Staff ${staff}</div>
                                    <div class="log-packages">${data.trips} trips</div>
                                </div>
                                <div class="log-details">
                                    Moved ${data.packages} packages today
                                </div>
                            </div>
                        </div>
                    `;
                    rank++;
                }
            });
            
            if (rank === 1) {
                leaderboardHTML = '<p style="text-align: center; color: #999; padding: 20px;">No trips logged yet today</p>';
            }
            
            leaderboardContainer.innerHTML = leaderboardHTML;
        }
        
        // Update activity log
        function updateActivityLog(filterType = currentFilter) {
            currentFilter = filterType;
            const activityLog = document.getElementById('activityLog');
            const today = new Date().toISOString().split('T')[0];
            
            let filteredTrips = [...haulageData.trips];
            
            if (filterType === 'today') {
                filteredTrips = filteredTrips.filter(trip => trip.date === today);
            }
            
            // Sort by most recent first
            filteredTrips.sort((a, b) => new Date(b.fullTime) - new Date(a.fullTime));
            
            if (filteredTrips.length === 0) {
                activityLog.innerHTML = `
                    <div style="text-align: center; padding: 40px 20px; color: #999;">
                        <i class="fas fa-clipboard-list" style="font-size: 48px; margin-bottom: 15px;"></i>
                        <p>No trips logged ${filterType === 'today' ? 'today' : 'yet'}</p>
                    </div>
                `;
                return;
            }
            
            let logHTML = '';
            filteredTrips.forEach(trip => {
                const isToday = trip.date === today;
                logHTML += `
                    <div class="log-entry" style="border-left-color: ${getStaffColor(trip.staff)};">
                        <div class="log-icon" style="background: ${getStaffColor(trip.staff)};">
                            ${trip.staff}
                        </div>
                        <div class="log-content">
                            <div class="log-header">
                                <div class="log-staff">Staff ${trip.staff} - Trip ${trip.tripNumber}</div>
                                <div class="log-time">
                                    ${isToday ? 'Today' : trip.date} ${trip.time}
                                </div>
                            </div>
                            <div class="log-details">
                                ${trip.packages} packages from ${trip.location}
                                ${!isToday ? `<span style="margin-left: 10px; font-size: 12px; color: #999;">(${trip.date})</span>` : ''}
                            </div>
                        </div>
                    </div>
                `;
            });
            
            activityLog.innerHTML = logHTML;
        }
        
        // Filter activity
        function filterActivity(filterType) {
            updateActivityLog(filterType);
            showNotification(`Showing ${filterType === 'today' ? "today's" : 'all'} activity`);
        }
        
        // Generate QR codes
        function generateQRCodes() {
            const qrcodesDiv = document.getElementById('qrcodes');
            let qrHTML = '';
            
            // Simple QR code simulation - in a real app, you'd use a QR code library
            ['A', 'B', 'C', 'D', 'E', 'F'].forEach(staff => {
                qrHTML += `
                    <div style="text-align: center; padding: 15px; background: #f5f5f5; border-radius: 10px;">
                        <div style="width: 100px; height: 100px; margin: 0 auto 10px; background: #e0e0e0; display: flex; align-items: center; justify-content: center; border-radius: 10px;">
                            <div style="font-size: 24px; font-weight: bold; color: ${getStaffColor(staff)};">
                                ${staff}
                            </div>
                        </div>
                        <div style="font-weight: bold; margin-bottom: 5px;">Staff ${staff}</div>
                        <div style="font-size: 12px; color: #666;">Scan to log trip</div>
                    </div>
                `;
            });
            
            qrcodesDiv.innerHTML = qrHTML;
        }
        
        // Generate PIN settings UI
        function generatePinSettings() {
            const pinSettingsDiv = document.getElementById('pinSettings');
            let pinHTML = '';
            
            ['A', 'B', 'C', 'D', 'E', 'F'].forEach(staff => {
                pinHTML += `
                    <div class="setting-item">
                        <div>
                            <strong>Staff ${staff} PIN</strong>
                        </div>
                        <input type="password" 
                               id="pin-${staff}" 
                               value="${haulageData.staffPins[staff]}" 
                               style="width: 80px; padding: 8px; text-align: center;"
                               onchange="updatePin('${staff}', this.value)">
                    </div>
                `;
            });
            
            pinSettingsDiv.innerHTML = pinHTML;
        }
        
        // Update PIN
        function updatePin(staff, newPin) {
            haulageData.staffPins[staff] = newPin;
            saveData();
            showNotification(`PIN updated for Staff ${staff}`);
        }
        
        // Save all data
        function saveData() {
            // Update settings
            haulageData.settings.pinProtection = document.getElementById('pinProtection').checked;
            haulageData.settings.dailyReset = document.getElementById('dailyReset').checked;
            
            localStorage.setItem('haulageData', JSON.stringify(haulageData));
        }
        
        // Export data
        function exportData() {
            const dataStr = JSON.stringify(haulageData, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = `haulage-data-${new Date().toISOString().split('T')[0]}.json`;
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showNotification('Data exported successfully!');
        }
        
        // Reset today's data
        function resetDailyData() {
            if (confirm('Are you sure you want to reset today\'s data? This cannot be undone.')) {
                const today = new Date().toISOString().split('T')[0];
                haulageData.trips = haulageData.trips.filter(trip => trip.date !== today);
                saveData();
                updateAllDisplays();
                showNotification("Today's data has been reset");
            }
        }
        
        // Clear all data
        function clearAllData() {
            if (confirm('Are you sure you want to clear ALL data? This cannot be undone.')) {
                haulageData.trips = [];
                saveData();
                updateAllDisplays();
                showNotification('All data has been cleared');
            }
        }
        
        // Check for daily reset
        function checkDailyReset() {
            if (!haulageData.settings.dailyReset) return;
            
            const today = new Date().toISOString().split('T')[0];
            if (haulageData.date !== today) {
                // New day - could add auto-reset here if desired
                haulageData.date = today;
                saveData();
                
                // Show notification about new day
                setTimeout(() => {
                    showNotification(`New day started! Ready to track trips for ${today}`);
                }, 1000);
            }
        }
        
        // Helper function to get staff color
        function getStaffColor(staff) {
            const colors = {
                'A': '#FF5722',
                'B': '#2196F3',
                'C': '#4CAF50',
                'D': '#FFC107',
                'E': '#9C27B0',
                'F': '#795548'
            };
            return colors[staff] || '#757575';
        }
        
        // Show notification
        function showNotification(message) {
            // Create notification element
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background: #4CAF50;
                color: white;
                padding: 15px 20px;
                border-radius: 10px;
                box-shadow: 0 5px 15px rgba(0,0,0,0.2);
                z-index: 1000;
                animation: slideInRight 0.3s, fadeOut 0.3s 2.7s;
                max-width: 300px;
                font-weight: 600;
            `;
            
            // Add keyframes for animations
            const style = document.createElement('style');
            style.textContent = `
                @keyframes slideInRight {
                    from { transform: translateX(100%); opacity: 0; }
                    to { transform: translateX(0); opacity: 1; }
                }
                @keyframes fadeOut {
                    from { opacity: 1; }
                    to { opacity: 0; }
                }
            `;
            document.head.appendChild(style);
            
            notification.innerHTML = `<i class="fas fa-check-circle" style="margin-right: 10px;"></i> ${message}`;
            document.body.appendChild(notification);
            
            // Remove after 3 seconds
            setTimeout(() => {
                if (notification.parentNode) {
                    notification.parentNode.removeChild(notification);
                }
            }, 3000);
        }
        
        // Auto-save settings
        document.getElementById('pinProtection').addEventListener('change', saveData);
        document.getElementById('dailyReset').addEventListener('change', saveData);
    </script>
</body>
</html>

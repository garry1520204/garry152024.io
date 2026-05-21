html<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Call Detail Record (CDR) Location Analysis Report</title>
    <style>
        :root {
            --primary-color: #1e293b;
            --secondary-color: #0f172a;
            --accent-color: #2563eb;
            --text-color: #334155;
            --light-bg: #f8fafc;
            --border-color: #e2e8f0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: var(--light-bg);
            color: var(--text-color);
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 25px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            margin: 0;
            font-size: 24px;
            letter-spacing: 0.5px;
        }

        .case-summary {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 15px;
            margin-top: 15px;
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 6px;
        }

        .summary-item span {
            display: block;
            font-size: 12px;
            color: #cbd5e1;
            text-transform: uppercase;
        }

        .summary-item strong {
            font-size: 16px;
            color: #ffffff;
        }

        .card {
            background: white;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1);
            margin-bottom: 25px;
        }

        .card-title {
            font-size: 18px;
            font-weight: 600;
            color: var(--secondary-color);
            margin-top: 0;
            margin-bottom: 15px;
            border-bottom: 2px solid var(--light-bg);
            padding-bottom: 10px;
        }

        .table-responsive {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            text-align: left;
            font-size: 14px;
        }

        th {
            background-color: var(--light-bg);
            color: var(--secondary-color);
            font-weight: 600;
            padding: 12px 10px;
            border-bottom: 2px solid var(--border-color);
        }

        td {
            padding: 12px 10px;
            border-bottom: 1px solid var(--border-color);
            white-space: nowrap;
        }

        tr:hover {
            background-color: #f1f5f9;
        }

        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 500;
            text-align: center;
        }

        .badge-incoming { background-color: #dcfce7; color: #15803d; }
        .badge-outgoing { background-color: #dbeafe; color: #1d4ed8; }
        .badge-sms { background-color: #fef9c3; color: #a16207; }

        .btn-map {
            display: inline-flex;
            align-items: center;
            background-color: var(--accent-color);
            color: white;
            padding: 6px 12px;
            font-size: 12px;
            font-weight: 500;
            text-decoration: none;
            border-radius: 4px;
            transition: background-color 0.2s;
        }

        .btn-map:hover {
            background-color: #1d4ed8;
        }

        .btn-map::before {
            content: "📍";
            margin-right: 4px;
        }
    </style>
</head>
<body>

<div class="container">

    <!-- Header & Investigation Summary -->
    <header>
        <h1>CDR Location Intelligence Analytics</h1>
        <div class="case-summary">
            <div class="summary-item">
                <span>Case Reference</span>
                <strong>CASE-2026-89A</strong>
            </div>
            <div class="summary-item">
                <span>Target Mobile Number</span>
                <strong>+91 98765 43210</strong>
            </div>
            <div class="summary-item">
                <span>Target IMEI / IMSI</span>
                <strong>86023404... / 40445...</strong>
            </div>
            <div class="summary-item">
                <span>Service Provider</span>
                <strong>Jio Telecom (Punjab Circle)</strong>
            </div>
        </div>
    </header>

    <!-- Geographic Location Analysis Grid -->
    <div class="card">
        <div class="card-title">Cell Tower Log & Spatial Footprint</div>
        <div class="table-responsive">
            <table>
                <thead>
                    <tr>
                        <th>Date & Time</th>
                        <th>Call Type</th>
                        <th>Dialled/Received Party</th>
                        <th>Duration</th>
                        <th>Cell ID (CID)</th>
                        <th>LAC / TAC</th>
                        <th>Tower Physical Address</th>
                        <th>Coordinates (Lat, Long)</th>
                        <th>Map Link</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- Entry 1 -->
                    <tr>
                        <td>2026-05-21 09:14:22</td>
                        <td><span class="badge badge-outgoing">Outgoing</span></td>
                        <td>+91 98765 00112</td>
                        <td>02:15 Min</td>
                        <td>43211</td>
                        <td>5612</td>
                        <td>Phase 8B, Industrial Area, Mohali</td>
                        <td>30.7114, 76.6912</td>
                        <td><a href="https://google.com" target="_blank" class="btn-map">View Map</a></td>
                    </tr>
                    <!-- Entry 2 -->
                    <tr>
                        <td>2026-05-21 11:30:05</td>
                        <td><span class="badge badge-incoming">Incoming</span></td>
                        <td>+91 98765 00155</td>
                        <td>00:45 Min</td>
                        <td>43215</td>
                        <td>5612</td>
                        <td>Sector 62, Near Library, Mohali</td>
                        <td>30.7241, 76.7104</td>
                        <td><a href="https://google.com" target="_blank" class="btn-map">View Map</a></td>
                    </tr>
                    <!-- Entry 3 -->
                    <tr>
                        <td>2026-05-21 14:02:10</td>
                        <td><span class="badge badge-sms">SMS Record</span></td>
                        <td>+91 98765 99887</td>
                        <td>-</td>
                        <td>88412</td>
                        <td>5930</td>
                        <td>Sirhind Road, Near Bara Phool, Punjab</td>
                        <td>30.6558, 76.4883</td>
                        <td><a href="https://google.com" target="_blank" class="btn-map">View Map</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>

</div>

</body>
</html>

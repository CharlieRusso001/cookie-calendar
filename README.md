# Cookie-Powered Calendar

A modern, interactive web-based calendar application that stores all event data directly in browser cookies. No server required, no database needed - your calendar data stays completely local and private.

## How It Works

### Data Storage
The calendar uses browser cookies to store event data with the following benefits:
- **Client-side only**: Your data never leaves your device
- **Automatic persistence**: Data survives browser restarts and system reboots
- **Size management**: Automatically handles cookie size limits by chunking large datasets
- **Secure**: Data is stored locally with standard browser security

### Cookie Structure
- Base namespace: `cpc_v2` (Cookie-Powered Calendar version 2)
- Chunk counter: `cpc_v2__count` - stores the number of data chunks
- Data chunks: `cpc_v2__0`, `cpc_v2__1`, etc. - actual event data
- Maximum chunk size: 3.5KB (well under browser 4KB limit)
- Expiration: 365 days

## Usage

### Managing Events
- **Add Event**: Select a date, fill the form, and submit
- **Edit Event**: Click the "Edit" button on any existing event
- **Delete Event**: Click the "Delete" button on any event
- **View Events**: Event badges appear on calendar days with events

### Navigation
- **Month Navigation**: Use arrow buttons or keyboard shortcuts (Ctrl/Cmd + Left/Right)
- **Jump to Today**: Click the "Today" button
- **Select Date**: Click any calendar day to view/edit events

### Data Management
- **Export**: Click "Export" to download your calendar as a JSON file
- **Import**: Click "Import" and select a previously exported JSON file
- **Clear All**: Remove all events (with confirmation dialog)

## Limitations

- **Cookie Storage**: Limited to approximately 4KB per cookie (handled automatically with chunking)
- **Browser Specific**: Data is tied to the specific browser and domain
- **Local Only**: No synchronization across devices or browsers
- **Cookie Policies**: Subject to browser cookie settings and policies

## Privacy & Security

- **No Server Communication**: All data processing happens locally
- **No Tracking**: No analytics, cookies, or external requests
- **Private by Design**: Your calendar data remains on your device
- **HTTPS Recommended**: Use HTTPS when hosting to enable secure cookie flags

## Technical Implementation

### Architecture
- **Single File Application**: Everything contained in one HTML file
- **Progressive Enhancement**: Works without JavaScript for basic viewing
- **Modern CSS**: Uses CSS Grid, Flexbox, and custom properties
- **Vanilla JavaScript**: No framework dependencies

## License

This project is open source. See LICENSE file for details.

# 🎙️ Record → n8n → Play 🎵

A beautiful, professional standalone HTML application for recording audio, sending it to n8n webhooks, and playing back the response. Transform your voice into magic with n8n workflows! ✨

## 📋 Table of Contents

- [Features](#-features)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Technical Details](#-technical-details)
- [Browser Compatibility](#-browser-compatibility)
- [Troubleshooting](#-troubleshooting)
- [File Structure](#-file-structure)

## ✨ Features

### 🎨 Visual Design

- **Animated Gradient Background** 🌈
  - Smooth color-shifting gradient animation
  - Professional purple-to-blue color scheme
  - Eye-catching visual appeal

- **Glassmorphism UI** 💎
  - Frosted glass effect cards with backdrop blur
  - Hover animations and smooth transitions
  - Modern, clean interface design

- **Gradient Buttons** 🎯
  - Beautiful gradient color schemes
  - Ripple effect on hover
  - Smooth animations and transitions
  - Disabled state handling

### 🎤 Audio Recording

- **Real-time Recording** 🎙️
  - Browser-based audio recording using MediaRecorder API
  - WebM audio format support
  - Microphone permission handling
  - Visual recording indicator with pulsing animation

- **Recording Timer** ⏱️
  - Live timer showing recording duration (MM:SS format)
  - Accurate time tracking
  - Visual pulse indicator during recording

- **Local Preview** 🎧
  - Instant playback of recorded audio
  - Standard HTML5 audio controls
  - Preview before sending to n8n

### ☁️ n8n Integration

- **Webhook Support** 🔗
  - Easy webhook URL configuration
  - FormData file upload
  - POST request handling
  - Error handling and validation

- **Progress Tracking** 📊
  - Animated progress bar during upload
  - Real-time progress updates
  - Visual feedback for processing stages
  - Shimmer animation effect

- **Response Handling** 🎵
  - Automatic audio response detection
  - JSON response parsing support
  - Audio URL extraction from JSON
  - Multiple response format support

### 📈 Statistics & Tracking

- **Statistics Dashboard** 📊
  - Total recordings count
  - Success rate tracking
  - Total recording time accumulation
  - Beautiful gradient stat cards

- **Workflow Visualization** 🔄
  - Step-by-step workflow indicator
  - Record → Send → Play visualization
  - Active step highlighting with bounce animation
  - Completed step indicators
  - Visual progress through workflow

### 🎯 Status & Feedback

- **Color-Coded Status Messages** 💬
  - **Idle**: Gray gradient - Ready state
  - **Recording**: Yellow gradient - Active recording
  - **Processing**: Blue gradient - Upload/processing
  - **Success**: Green gradient - Operation successful
  - **Error**: Red gradient - Error occurred

- **Emoji-Rich Interface** 😊
  - Emojis throughout the interface
  - Visual indicators for all actions
  - Friendly, approachable design
  - Clear visual communication

### 🎮 User Experience

- **Smart Button States** 🎛️
  - Context-aware button enabling/disabling
  - Visual feedback for available actions
  - Prevents invalid operations

- **Audio Badges** 🏷️
  - Preview badge for local recording
  - Response badge for n8n audio
  - Visual distinction between audio sources

- **Responsive Design** 📱
  - Works on desktop and mobile devices
  - Flexible layout with CSS Grid
  - Adaptive button wrapping
  - Mobile-friendly interface

- **Viewport-Optimized Layout** 🖥️
  - Single viewport design - all content visible without scrolling
  - Compact spacing and sizing for maximum efficiency
  - Audio players displayed side-by-side in grid layout
  - Statistics in compact 3-column grid
  - Optimized for standard browser window sizes

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, Safari)
- Microphone access permissions
- An n8n webhook URL

### Installation

1. Download or clone the `voice.html` file
2. Open it in your web browser
3. No additional setup required - it's a standalone file!

### First Use

1. **Grant Microphone Permission** 🎤
   - When prompted, click "Allow" to grant microphone access
   - This is required for audio recording

2. **Enter Webhook URL** 🔗
   - Paste your n8n webhook URL in the input field
   - Use test URL during development
   - Switch to production URL when ready

3. **Start Recording** 🎙️
   - Click "Start Recording" button
   - Speak into your microphone
   - Watch the timer and recording indicator

4. **Stop Recording** ⏹️
   - Click "Stop" when finished
   - Preview your recording locally

5. **Send to n8n** ☁️
   - Click "Send to n8n" button
   - Watch the progress bar
   - Wait for response

6. **Play Response** 🎵
   - Response audio will appear automatically
   - Click play to hear the result

## 📖 Usage

### Recording Audio

1. Click the **🎤 Start Recording** button
2. Speak into your microphone
3. Watch the timer count up (MM:SS format)
4. Click **⏹️ Stop** when finished
5. Preview your recording using the audio player

### Sending to n8n

1. Ensure you have a recording ready
2. Verify your webhook URL is entered
3. Click **☁️ Send to n8n** button
4. Monitor the progress bar
5. Wait for the response

### Understanding the Workflow

The application visualizes a 3-step workflow:

1. **🎤 Record** - Record your audio
2. **☁️ Send** - Send to n8n webhook
3. **🎵 Play** - Play the response

Each step highlights when active and shows completion status.

### Layout Features

The application features a compact, viewport-optimized design:
- **Single Viewport**: All content fits in one browser window without scrolling
- **Grid Layout**: Audio players displayed side-by-side for efficient space usage
- **Compact Statistics**: Three-column grid showing recordings, success count, and total time
- **Responsive Elements**: All components sized appropriately for the viewport
- **Fixed Footer**: Disclaimer always visible at the bottom

### Statistics

The statistics dashboard shows:
- **📊 Recordings**: Total number of recordings made
- **✅ Success**: Number of successful n8n responses
- **⏱️ Total Time**: Cumulative recording time in seconds

## 🔧 Technical Details

### Technologies Used

- **HTML5**: Structure and semantic markup
- **CSS3**: 
  - CSS Grid and Flexbox for layout
  - CSS Animations and Transitions
  - CSS Gradients
  - Backdrop Filter (glassmorphism)
- **JavaScript (ES6+)**:
  - MediaRecorder API for audio recording
  - Fetch API for HTTP requests
  - DOM manipulation
  - Event handling

### Audio Format

- **Recording Format**: WebM (audio/webm)
- **Browser Support**: All modern browsers
- **Codec**: Browser default (typically Opus)

### API Integration

The application sends audio to n8n using:
- **Method**: POST
- **Content-Type**: multipart/form-data
- **Field Name**: `audio`
- **File Name**: `recording.webm`

### Response Handling

The application handles multiple response types:
1. **Direct Audio**: Audio MIME types (audio/*)
2. **JSON with Audio URL**: `{ "audioUrl": "..." }` or `{ "audio": "..." }`
3. **Error Responses**: HTTP error status codes

## 🌐 Browser Compatibility

### Fully Supported
- ✅ Chrome 47+
- ✅ Firefox 25+
- ✅ Edge 79+
- ✅ Safari 14.1+
- ✅ Opera 34+

### Required Features
- MediaRecorder API
- Fetch API
- CSS Grid
- Backdrop Filter (for glassmorphism effect)

### Known Limitations
- Some older browsers may not support backdrop-filter (glassmorphism will fall back to solid background)
- Safari may require HTTPS for microphone access in some cases

## 🔍 Troubleshooting

### Microphone Not Working

**Problem**: Can't access microphone
- **Solution**: Check browser permissions
  - Chrome: Settings → Privacy → Site Settings → Microphone
  - Firefox: Preferences → Privacy → Permissions → Microphone
  - Safari: Safari → Preferences → Websites → Microphone

### Webhook Not Responding

**Problem**: Error sending to n8n
- **Check**: Verify webhook URL is correct
- **Check**: Ensure n8n workflow is active
- **Check**: Verify CORS settings if needed
- **Check**: Check browser console for detailed errors

### No Audio Response

**Problem**: Response received but no audio
- **Check**: n8n workflow returns audio file
- **Check**: Response format matches expected types
- **Check**: Audio file is valid format
- **Check**: Check browser console for errors

### Progress Bar Not Showing

**Problem**: Progress bar doesn't appear
- **Solution**: This is normal - progress bar only shows during upload/processing
- **Note**: Progress is simulated for visual feedback

### Statistics Not Updating

**Problem**: Stats don't increment
- **Solution**: Statistics update after recording stops and after successful responses
- **Note**: Stats reset on page refresh (stored in memory only)

## 📁 File Structure

```
week2day2chp36/
├── voice.html          # Main application file (standalone)
└── README.md          # This documentation file
```

### File Details

- **voice.html**: Complete standalone application
  - All HTML, CSS, and JavaScript in one file
  - No external dependencies
  - No build process required
  - Ready to use immediately
  - Viewport-optimized layout
  - Includes disclaimer footer with author information

## 🎨 Customization

### Changing Colors

Edit the CSS gradient values in the `<style>` section:
- Background gradient: `body` background property
- Button gradients: `.btn-primary`, `.btn-secondary`, `.btn-success`
- Card colors: `.card` background property

### Modifying Animations

Adjust animation timings in CSS:
- `@keyframes gradientShift`: Background animation speed
- `@keyframes pulse`: Recording indicator pulse speed
- `@keyframes bounce`: Step indicator bounce animation

### Adding Features

The code is well-structured and easy to extend:
- Add new buttons in the `.buttons` container
- Add new status types in the `.status` class
- Extend statistics in the `stats` object

## 📝 Notes

- **Standalone**: No server required - works directly from file system
- **No Dependencies**: Pure HTML, CSS, and JavaScript
- **Privacy**: All processing happens in your browser
- **Offline**: Works offline (except for n8n webhook calls)
- **Portable**: Single file - easy to share and deploy
- **Viewport-Optimized**: Designed to fit in a single browser viewport without scrolling
- **Compact Layout**: Efficient use of space with optimized sizing and spacing

## 🎉 Tips & Best Practices

1. **Test URL First** 💡
   - Use test webhook URL during development
   - Switch to production when ready

2. **Check Permissions** 🔒
   - Grant microphone access when prompted
   - Check browser settings if issues occur

3. **Monitor Console** 🖥️
   - Open browser DevTools for debugging
   - Check Network tab for webhook calls
   - Review Console for error messages

4. **Test Audio Quality** 🎵
   - Preview recordings before sending
   - Ensure good microphone positioning
   - Check audio levels

5. **Workflow Visualization** 👀
   - Watch the workflow steps for progress
   - Active steps bounce, completed steps are highlighted
   - Use as visual feedback

## 🚀 Future Enhancements

Potential features for future versions:
- [ ] Audio format selection (MP3, WAV, etc.)
- [ ] Audio quality settings
- [ ] Download recorded audio
- [ ] Save statistics to localStorage
- [ ] Multiple webhook profiles
- [ ] Audio visualization (waveform)
- [ ] Keyboard shortcuts
- [ ] Dark mode toggle
- [ ] Export statistics
- [ ] Audio trimming/editing

## ⚠️ Disclaimer

This application is provided "as is" without warranty of any kind. Use at your own risk.

**Created by:** Lalit Nayyar  
**Contact:** [lalitnayyar@gmail.com](mailto:lalitnayyar@gmail.com)

The application is provided for educational and development purposes. The author is not responsible for any issues, data loss, or problems that may arise from using this application.

## 📄 License

This is a standalone educational project. Feel free to use, modify, and distribute as needed.

## 🙏 Credits

**Author:** Lalit Nayyar  
**Email:** [lalitnayyar@gmail.com](mailto:lalitnayyar@gmail.com)

Created with ❤️ using modern web technologies:
- HTML5 MediaRecorder API
- CSS3 Animations & Gradients
- JavaScript ES6+
- n8n Integration

---

**Enjoy recording and transforming your voice with n8n! 🎙️✨🎵**

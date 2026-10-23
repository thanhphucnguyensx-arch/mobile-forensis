# TrueVision AI - Deepfake Detection & Forensics

A professional web application for detecting deepfakes, image manipulation, and digital forensics analysis. Built with modern web technologies and optimized for international 5-star standards.

## 🌟 Key Features

### Core Functionality
- **Multi-Media Support**: Analyze images, videos, and audio files
- **Real Forensics Analysis**: EXIF metadata extraction, file hash verification, anomaly detection
- **Hybrid AI Architecture**: Client-side analysis with server-side AI integration capability
- **Professional PDF Reports**: Generate detailed forensic analysis certificates
- **Local History**: Track all analysis results locally (privacy-first)

### User Experience
- **Multi-Language Support**: Vietnamese, English, Chinese, Spanish
- **Modern UI/UX**: Glass morphism design, smooth animations, loading states
- **Responsive Design**: Optimized for mobile, tablet, and desktop
- **Accessibility**: ARIA labels, keyboard navigation, screen reader support
- **Error Handling**: Graceful degradation with clear error messages

### Technical Excellence
- **PWA Ready**: Installable as a standalone app with offline support
- **Performance**: Lazy loading, optimized asset loading, fast analysis
- **Privacy-First**: All data processed locally, no unnecessary data collection
- **Security**: File validation, size limits, secure hash calculation

## 🚀 Getting Started

### Quick Start

1. **Open the Application**
   - Simply open `truevision-ai.html` in a modern web browser
   - For best experience, use Chrome, Firefox, Safari, or Edge

2. **Upload Media**
   - Click the upload area or drag & drop a file
   - Supported formats: Images (JPG, PNG, WEBP), Videos (MP4, WEBM), Audio (MP3, WAV)
   - Maximum file size: 50MB

3. **Analyze**
   - Click "Analyze" to start forensic analysis
   - Wait for the analysis to complete (typically 2-3 seconds)
   - View detailed results including AI score, anomaly level, and EXIF data

4. **Export Report**
   - Click "Export PDF" to generate a professional forensic certificate
   - PDF includes all analysis details, metadata, and detected factors

### PWA Installation

To install as a standalone app:

1. Open the app in Chrome or Edge
2. Click the install icon in the address bar
3. Follow the prompts to install
4. The app will work offline after first load

## 🔧 Configuration

### Server-Side AI Integration

The app uses a hybrid architecture:
- **Client-side**: EXIF analysis, file hash, basic forensics (always available)
- **Server-side**: Advanced AI deepfake detection (requires backend setup)

To enable server-side AI:

1. Set up your AI analysis backend
2. Update the `API_ENDPOINT` in `truevision-ai.html` (line ~730):
   ```javascript
   const API_ENDPOINT = 'https://your-api-domain.com/analyze';
   ```
3. Add authentication if needed:
   ```javascript
   headers: {
     'Authorization': 'Bearer YOUR_API_KEY'
   }
   ```
4. Uncomment the server AI code block in `analyzeWithServerAI()` function

### Customization

#### Languages
Add new languages in the `I18N` object (line ~220):
```javascript
const I18N = {
  // existing languages...
  fr: {
    header_sub: "Détection de Deepfake et Forensique",
    // add all translations...
  }
};
```

#### Analysis Thresholds
Adjust detection thresholds in `basicForensicsAnalysis()` (line ~620):
```javascript
if (result.aiScore > 60) {
  // Consider as fake
} else if (result.aiScore < 30) {
  // Consider as real
} else {
  // Uncertain
}
```

## 📊 Analysis Metrics

### AI Deepfake Index
- **0-30%**: Likely authentic (low manipulation probability)
- **30-60%**: Uncertain (needs higher quality file)
- **60-100%**: Likely manipulated (high deepfake probability)

### Anomaly Levels
- **Low**: Natural patterns detected
- **Medium**: Some irregularities found
- **High**: Significant anomalies detected

### Forensics Factors
The app checks for:
- Missing EXIF metadata
- Screenshot indicators
- Unusual file sizes
- Old file modification dates
- Inconsistent compression patterns

## 🔒 Privacy & Security

### Data Handling
- **Local Processing**: All analysis happens in your browser
- **No Cloud Storage**: Files are not uploaded or stored
- **Local History**: Analysis history stored in browser localStorage
- **Optional Server AI**: Only sends data if server AI is configured

### Best Practices
- Always use original, high-quality files for accurate results
- Screenshots may show as "uncertain" due to compression artifacts
- EXIF data can be edited - use multiple analysis methods
- Results are for informational purposes, not legal evidence

## 🌐 Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ⚠️ IE: Not supported

## 📱 PWA Features

When installed as a PWA:
- Works offline (after first load)
- Faster startup times
- Full-screen experience
- Home screen icon
- Background sync capability

## 🐛 Troubleshooting

### Analysis fails
- Check file size (max 50MB)
- Ensure file format is supported
- Try a different browser
- Clear browser cache

### PDF export fails
- Check browser permissions
- Ensure html2pdf library loaded
- Try reducing file size

### PWA won't install
- Use Chrome or Edge
- Ensure HTTPS (or localhost)
- Check browser settings

## 🔄 Updates

### Client-Side Updates
Simply replace `truevision-ai.html` with the new version.

### Service Worker Updates
The service worker will auto-update when:
- You clear the cache
- The cache version changes (edit `CACHE_NAME` in service-worker.js)

## 📄 License

This project is for educational and informational purposes.

## ⚠️ Disclaimer

This tool provides forensic analysis for informational purposes only. Results should not be used as definitive legal evidence. Always consult with professional forensic experts for critical decisions.

## 🤝 Contributing

To contribute improvements:
1. Test thoroughly before making changes
2. Maintain the existing code style
3. Add appropriate error handling
4. Update documentation
5. Test across multiple browsers

## 📞 Support

For issues or questions:
- Check the troubleshooting section
- Review browser console for errors
- Ensure all external libraries are accessible

## 🎯 Roadmap

Future enhancements:
- [ ] TensorFlow.js integration for client-side ML
- [ ] Advanced Error Level Analysis (ELA)
- [ ] Video frame-by-frame analysis
- [ ] Audio deepfake detection
- [ ] Batch analysis support
- [ ] Cloud backup for history
- [ ] API for third-party integration
- [ ] Mobile native app (React Native)

---

**Built with ❤️ for digital security and truth verification**

# Vetsphere Viewer

Professional DICOM Medical Imaging Viewer built on OHIF (Open Health Imaging Foundation)

## 🐾 Features

- **DICOM Study Viewing**: Load and examine medical imaging studies
- **Advanced Tools**: Measurement, annotation, and analysis capabilities
- **Easy Integration**: Embed in your applications with iframe
- **OHIF Powered**: Built on the industry-standard OHIF platform
- **Veterinary Focused**: Designed for veterinary medical imaging

## 🚀 Quick Start

### View Online
Visit: [https://jayvet403.github.io/Vetsphere-viewer/](https://jayvet403.github.io/Vetsphere-viewer/)

### Open Viewer
Click "Open Viewer" button on the main page or go to: [https://jayvet403.github.io/Vetsphere-viewer/viewer.html](https://jayvet403.github.io/Vetsphere-viewer/viewer.html)

## 📱 Embedding

### Basic Embed
```html
<iframe 
  src="https://jayvet403.github.io/Vetsphere-viewer/viewer.html" 
  width="100%" 
  height="800" 
  frameborder="0">
</iframe>
```

### Load Specific Study
```html
<iframe 
  src="https://jayvet403.github.io/Vetsphere-viewer/viewer.html?studyInstanceUIDs=1.2.3.4.5" 
  width="100%" 
  height="800" 
  frameborder="0">
</iframe>
```

### PostMessage API
From your parent window, send messages to load studies:

```javascript
const frame = document.getElementById('viewer-iframe');
frame.contentWindow.postMessage({
  type: 'LOAD_STUDY',
  studyInstanceUID: '1.2.3.4.5'
}, '*');
```

## 📚 API Reference

### VetsphereViewerAPI
The viewer exposes a global API when loaded:

```javascript
// Load a study by UID
VetsphereViewerAPI.loadStudy('1.2.3.4.5');
```

### PostMessage Events
Listen for messages from the viewer (future enhancement):
```javascript
window.addEventListener('message', (event) => {
  if (event.data.type === 'VIEWER_READY') {
    console.log('Viewer is ready');
  }
});
```

## 🛠️ Technologies

- **OHIF Viewer**: https://viewer.ohif.org/
- **dcmjs**: DICOM web server support
- **Vanilla JavaScript**: No framework dependencies

## 📋 Browser Support

- Chrome/Chromium (Latest)
- Firefox (Latest)
- Safari (Latest)
- Edge (Latest)

## 📦 Files

- `index.html` - Main landing page
- `viewer.html` - DICOM viewer
- `embed-example.html` - Embedding examples
- `README.md` - Documentation

## 🔗 Resources

- [OHIF Viewer Documentation](https://docs.ohif.org/)
- [dcmjs Documentation](https://github.com/dcmjs-org/dcmjs)
- [DICOM Standard](https://www.dicomstandard.org/)

## 📝 License

MIT

## 🤝 Support

For issues or feature requests, please open an issue on GitHub.

---

**Vetsphere** - Veterinary Medical Imaging Platform 🐾

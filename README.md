# Image Slider

A responsive image slider built with React, TypeScript, and Tailwind CSS.

## Features

- Displays one image at a time with smooth transitions
- Navigation with Next and Previous buttons
- Keyboard navigation support (left/right arrow keys)
- Automatic slideshow with 5-second intervals
- Dot indicators showing current slide position
- Responsive design that works on all screen sizes
- Image preloading for smoother experience

## Technical Approach

### Component Structure

The image slider is built as a single React component that manages:

1. **State Management**: 
   - Uses React's `useState` hook to track the current slide index
   - Uses `useEffect` for side effects like auto-advancing slides and keyboard navigation

2. **Image Handling**:
   - Stores image URLs in an array
   - Preloads images to prevent flickering during transitions
   - Shows a loading indicator while images are being loaded

3. **Navigation**:
   - Circular navigation (wraps from last to first slide and vice versa)
   - Multiple navigation methods (buttons, keyboard, indicators)
   - Visual feedback on hover states

4. **Transitions**:
   - Uses CSS transitions for smooth fade effects between slides
   - Optimized for performance with z-index management

5. **Accessibility**:
   - Proper aria-labels for all interactive elements
   - Keyboard navigation support
   - Visual indicators of current state

### Styling

- Built with Tailwind CSS for responsive design
- Dark theme with high contrast for better visibility
- Responsive container that maintains aspect ratio
- Semi-transparent controls that become more visible on hover

### Performance Considerations

- Image preloading to prevent layout shifts
- Efficient state updates to minimize re-renders
- CSS transitions instead of JavaScript animations for better performance
- Proper cleanup of event listeners and intervals to prevent memory leaks

## Deployment

The application is deployed on Netlify, providing:
- Fast global CDN
- Automatic HTTPS
- Continuous deployment from the repository

## Future Improvements

Potential enhancements for the image slider:
- Swipe gestures for touch devices
- Customizable transition effects
- Caption support for images
- Lazy loading for better performance with many images
- Fullscreen mode
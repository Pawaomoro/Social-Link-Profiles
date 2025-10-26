# Social Links Profile

A responsive social media link-sharing profile card that allows users to showcase all their social media platforms in one clean, accessible location. Built as part of a Frontend Mentor challenge.



## Overview

### The Challenge

Build a social links profile component that:
- Displays a user profile with avatar and bio
- Lists multiple social media links in an organized manner
- Is fully responsive across all device sizes
- Provides interactive hover states
- Maintains clean and accessible design

##  Features

- Clean profile card design
- Multiple social media link buttons
- Hover effects on interactive elements
- Fully responsive layout
- Mobile-first approach
- Semantic HTML structure
- Accessible design

## 🛠 Built With

- HTML5
- CSS3
- Responsive design principles
- CSS custom properties (variables)
- Flexbox for layout

## 📚 What I Learned

This project was excellent for practicing responsive design techniques and understanding how to make components adapt gracefully across different screen sizes.

### Key Learnings

**1. CSS Box Model & Width Management**
```css
.card {
  min-width: 375px;  /* Prevents card from becoming too narrow */
  width: 100%;        /* Allows card to grow with container */
  max-width: 400px;   /* Prevents card from becoming too wide */
}
```

**2. Responsive Button Styling**
```css
.social-link {
  width: 100%;        /* Full width of parent container */
  padding: 1rem;      /* Consistent spacing */
  box-sizing: border-box; /* Includes padding in width calculation */
}
```

**3. Container Approach**
```css
.container {
  width: 100%;
  max-width: 1200px;
  padding: 0 1rem;    /* Prevents content from touching edges */
  margin: 0 auto;     /* Centers the container */
}
```

## 🚧 Challenges Faced

### Making the Profile Responsive

**Challenge**: Creating a profile card that looks great on all screen sizes from mobile phones (320px) to large desktop monitors (1920px+).

**Problem**: Initially, the card would either:
- Become too narrow on mobile devices, making text cramped
- Stretch too wide on desktop, looking unbalanced
- Have inconsistent spacing across different breakpoints

**Solution**: Implemented a flexible width strategy using `min-width` and `width: 100%`:

```css
.profile-card {
  min-width: 320px;   /* Minimum usable width */
  width: 100%;        /* Flexible width */
  max-width: 450px;   /* Maximum readable width */
  margin: 0 auto;     /* Center on larger screens */
  padding: 1.5rem;    /* Internal spacing */
}

/* Social links maintain consistent width */
.social-links {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.social-link {
  width: 100%;        /* Full width of parent */
  padding: 1rem;
  box-sizing: border-box;
}
```

**Key Takeaways**:
- `min-width` ensures content remains readable on small screens
- `width: 100%` allows the component to adapt to its container
- `max-width` prevents the design from breaking on large screens
- `box-sizing: border-box` ensures padding doesn't break the layout
- Using relative units (rem, %) instead of fixed pixels (px) improves scalability

**Why This Approach Works**:
1. **Mobile First**: Starts with 100% width, naturally fills small screens
2. **Controlled Growth**: `min-width` sets a comfortable minimum
3. **Prevents Over-expansion**: `max-width` keeps the card at optimal reading width
4. **No Media Queries Needed**: The card adapts automatically without breakpoints

## 📱 Responsive Design

The profile adapts seamlessly across devices:

- **Mobile (320px - 768px)**: Full-width card with comfortable touch targets
- **Tablet (768px - 1024px)**: Centered card with optimal reading width
- **Desktop (1024px+)**: Centered card maintains maximum width for readability



##  Installation

1. Clone the repository
```bash
git clone https://github.com/Pawaomoro/Social-Link-Profiles.git

2. Navigate to the project directory
```bash
cd social-links-profile
```

3. Open `index.html` in your browser
```bash
open index.html
```

## 🎨 Customization

You can easily customize this profile by:

1. **Changing colors**: Update CSS custom properties
```css
:root {
  --primary-color: black;
}
```

2. **Adding more links**: Add additional link buttons in the HTML
```html
<a href="#" class="social-link">Your Platform</a>
```

3. **Adjusting sizes**: Modify the `min-width` and `max-width` values to suit your needs

## 👤 Author

- GitHub - (https://github.com/Pawaomoro)
- Frontend Mentor -(https://www.frontendmentor.io/profile/Pawaomoro)
- LinkedIn - (https://www.linkedin.com/in/Eddie)

## 🙏 Acknowledgments

- Challenge provided by [Frontend Mentor](https://www.frontendmentor.io)
- Inspiration from modern link-in-bio platforms like Linktree
- Frontend Mentor community for feedback and support

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

**Note**: This project is for educational purposes and is based on a Frontend Mentor challenge.

## 🚀 Future Improvements

Potential enhancements for this project:
- [ ] Add smooth scroll animations
- [ ] Implement dark/light theme toggle
- [ ] Add social media icon SVGs
- [ ] Include analytics tracking
- [ ] Add share functionality
- [ ] Implement custom domain support

To view the portfolio:

1. Ensure you have installed all necessary dependencies with `npm install`.
2. Start the development server by running `npm run dev`.
3. Open your web browser and go to [http://localhost:5173](http://localhost:5173) to start exploring.



## 🎥 Framer Motion (Animations)

Framer Motion is a library that helps create animations in React applications. It makes designing animations simpler and more flexible than traditional CSS animations.

### Example of Framer Motion in This Portfolio

In this portfolio, Framer Motion adds smooth and engaging animations to improve how users interact with the site. Here’s how it’s used:

```javascript
// 🔄 Animation variants for motion components
const variants = {
  hidden: { translateX: '100px', opacity: 0 },
  visible: (delay: number) => ({
    translateX: '0px',
    opacity: 1,
    transition: {
      delay,
      type: 'spring',
      duration: 0.6,
    },
  }),
}

// 🎬 MotionBlock component to handle animations
const MotionBlock = ({ className, delay, children }: MotionBlockProps) => (
  <motion.div
    initial="hidden"
    animate="visible"
    variants={variants}
    className={className}
    custom={delay}
  >
    {children}
  </motion.div>
)
```

The code defines two key parts for animations using Framer Motion. The `variants` object specifies different animation states — `hidden` starts the component off-screen with reduced visibility, while `visible` brings it into view with smooth transitions based on a specified delay and spring physics for a natural feel. The `MotionBlock` component uses these variants to animate elements when they first appear, allowing each component to fade in and move into place at different times depending on the delay set.


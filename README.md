# Portfolio Website

A modern, interactive portfolio website built with Next.js, featuring smooth animations with GSAP, immersive 3D experiences with Three.js, and beautiful UI components from shadcn/ui.

## 🚀 Features

- **Modern Stack**: Built with Next.js 14+ for optimal performance and SEO
- **Cloud Database**: Snowflake data cloud for scalable data management
- **Smooth Animations**: GSAP-powered animations for engaging user interactions
- **3D Graphics**: Three.js integration for immersive visual experiences
- **Beautiful UI**: Consistent design system with shadcn/ui components
- **Responsive Design**: Fully responsive across all devices
- **Performance Optimized**: Fast loading times and smooth interactions
- **TypeScript**: Full type safety throughout the application

## 🛠️ Tech Stack

- **Framework**: [Next.js 14+](https://nextjs.org/)
- **Database**: [Snowflake](https://www.snowflake.com/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Animations**: [GSAP](https://greensock.com/gsap/)
- **3D Graphics**: [Three.js](https://threejs.org/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Icons**: [Lucide Icons](https://lucide.dev/)

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

Add your Snowflake credentials:
```env
SNOWFLAKE_ACCOUNT=your_account_identifier
SNOWFLAKE_USERNAME=your_username
SNOWFLAKE_PASSWORD=your_password
SNOWFLAKE_WAREHOUSE=your_warehouse
SNOWFLAKE_DATABASE=your_database
SNOWFLAKE_SCHEMA=your_schema
```

4. Run the development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🎨 Project Structure

```
├── app/                    # Next.js app directory
│   ├── api/               # API routes
│   │   └── snowflake/     # Snowflake database endpoints
│   ├── components/         # Reusable components
│   │   ├── ui/            # shadcn/ui components
│   │   ├── three/         # Three.js components
│   │   └── animations/    # GSAP animation components
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Root layout
│   └── page.tsx          # Home page
├── lib/                   # Utility functions
│   ├── utils.ts          # General utilities
│   ├── gsap.ts           # GSAP configurations
│   ├── three.ts          # Three.js utilities
│   └── snowflake.ts      # Snowflake database client
├── public/               # Static assets
│   ├── models/          # 3D models
│   ├── textures/        # Three.js textures
│   └── images/          # Images and icons
├── components.json       # shadcn/ui config
├── tailwind.config.js    # Tailwind configuration
├── .env.example         # Environment variables template
└── next.config.js        # Next.js configuration
```

## ⚡ Key Components

### Snowflake Integration
- Secure cloud data warehouse connectivity
- Real-time data analytics and insights
- Scalable data processing for portfolio metrics
- API endpoints for data visualization

### GSAP Animations
- Smooth page transitions
- Scroll-triggered animations
- Interactive hover effects
- Loading animations

### Three.js Integration
- Interactive 3D scenes
- Custom shaders and materials
- Responsive 3D canvas
- Performance optimized rendering

### shadcn/ui Components
- Consistent design system
- Accessible components
- Dark/light mode support
- Customizable themes

## 🔧 Configuration

### Snowflake Setup
Snowflake connection is configured in `lib/snowflake.ts` with:
- Secure credential management
- Connection pooling for performance
- Error handling and retry logic
- Query optimization utilities

### GSAP Setup
GSAP animations are configured in `lib/gsap.ts`. Key features include:
- ScrollTrigger for scroll-based animations
- Custom easing functions
- Responsive animation handling

### Three.js Configuration
Three.js setup is handled in `lib/three.ts` with:
- Scene optimization
- Responsive canvas handling
- Performance monitoring
- Asset loading utilities

### shadcn/ui Customization
UI components are configured in `components.json` and can be customized through:
- Tailwind theme extension
- CSS custom properties
- Component variants

## 📱 Responsive Design

The portfolio is fully responsive with breakpoints:
- Mobile: `< 768px`
- Tablet: `768px - 1024px`
- Desktop: `> 1024px`

## 🎯 Performance Optimizations

- **Database Optimization**: Snowflake query caching and result optimization
- **Image Optimization**: Next.js Image component with lazy loading
- **Code Splitting**: Dynamic imports for heavy components
- **3D Optimization**: LOD (Level of Detail) for Three.js models
- **Animation Performance**: GSAP's performant rendering
- **Bundle Analysis**: Webpack bundle analyzer integration
- **Data Caching**: Strategic caching for Snowflake queries

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your GitHub repository to Vercel
2. Configure environment variables (including Snowflake credentials)
3. Deploy automatically on push to main branch

**Required Environment Variables:**
```env
SNOWFLAKE_ACCOUNT=your_account_identifier
SNOWFLAKE_USERNAME=your_username
SNOWFLAKE_PASSWORD=your_password
SNOWFLAKE_WAREHOUSE=your_warehouse
SNOWFLAKE_DATABASE=your_database
SNOWFLAKE_SCHEMA=your_schema
```

### Other Platforms
The application can be deployed to any platform that supports Next.js:
- Netlify
- AWS Amplify
- Digital Ocean App Platform
- Railway

## 🔄 Development Workflow

1. **Development**: `npm run dev`
2. **Build**: `npm run build`
3. **Start Production**: `npm start`
4. **Lint**: `npm run lint`
5. **Type Check**: `npm run type-check`

## 📄 Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # Run TypeScript checks
npm run analyze      # Analyze bundle size
```

## 🎨 Customization

### Adding Database Queries
1. Create new API routes in `app/api/snowflake/`
2. Use Snowflake client from `lib/snowflake.ts`
3. Implement proper error handling and data validation

### Adding New Animations
1. Create animation functions in `lib/gsap.ts`
2. Use GSAP hooks in components
3. Configure ScrollTrigger for scroll-based animations

### Adding 3D Elements
1. Import models into `public/models/`
2. Create Three.js components in `components/three/`
3. Integrate with React using `useEffect` and `useRef`

### Styling
- Modify `tailwind.config.js` for theme customization
- Add custom CSS in `app/globals.css`
- Use shadcn/ui theme variables for consistency

## 🐛 Troubleshooting

### Common Issues

**Snowflake connection errors**
- Verify environment variables are correctly set
- Check network connectivity and firewall settings
- Ensure Snowflake account identifier format is correct
- Validate user permissions and warehouse access

**GSAP ScrollTrigger not working**
- Ensure ScrollTrigger is registered: `gsap.registerPlugin(ScrollTrigger)`
- Refresh ScrollTrigger on route changes

**Three.js performance issues**
- Use `dispose()` methods to clean up resources
- Implement LOD for complex models
- Monitor frame rate with stats.js

**shadcn/ui components not styled**
- Verify Tailwind CSS is properly configured
- Check if components are imported correctly
- Ensure CSS variables are defined

## 📚 Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Snowflake Documentation](https://docs.snowflake.com/)
- [GSAP Documentation](https://greensock.com/docs/)
- [Three.js Documentation](https://threejs.org/docs/)
- [shadcn/ui Documentation](https://ui.shadcn.com/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature/new-feature`
5. Submit a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js Team](https://nextjs.org/) for the amazing framework
- [Snowflake](https://www.snowflake.com/) for the powerful data cloud platform
- [GreenSock](https://greensock.com/) for powerful animations
- [Three.js Team](https://threejs.org/) for 3D capabilities
- [shadcn](https://twitter.com/shadcn) for beautiful UI components

---

**Built with ❤️ by [Nhatphanhk102]**

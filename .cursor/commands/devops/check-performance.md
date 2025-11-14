# Check Performance

Checks how fast your website is and finds ways to make it faster. Tests page load times, bundle sizes, and Core Web Vitals to make sure your site is fast for users.

1. **Check performance metrics**
   - Check Core Web Vitals (LCP, FID/INP, CLS)
   - Check bundle sizes (JavaScript, CSS)
   - Check page load times
   - Check image sizes and optimization
   - Check for performance issues
   - Tell the user what you found

2. **Identify performance problems**
   - Find slow pages or components
   - Find large bundles that slow down loading
   - Find unoptimized images
   - Find blocking resources
   - Find performance bottlenecks
   - Tell the user what's slowing things down

3. **Fix performance issues**
   - Optimize images (use next/image, proper sizing)
   - Code-split large bundles
   - Lazy load below-the-fold content
   - Optimize Server Components usage
   - Remove unused code
   - Optimize database queries (if applicable)
   - Fix performance problems

4. **Verify improvements**
   - Check performance metrics again
   - Make sure improvements worked
   - Confirm site is faster
   - Show before/after comparison

5. **Document performance check**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/performance-check-YYYY-MM-DD.md`
   - Document: issues found, fixes applied, performance improvements, metrics

## What to Tell the User

- Explain you're checking how fast their website is
- List what you're checking (page load times, bundle sizes, Core Web Vitals)
- Show performance metrics and identify problems
- Fix performance issues step by step
- Show improvements and before/after comparison
- Tell them when performance checks pass
- Document all checks and improvements

## See Also

### Workflow
- **[Maintain](../engineer/maintain.md)**: Advanced maintenance command
- **[Deploy](../deploy.md)**: Deploy after performance optimization
- **[Build](../build.md)**: Build performance optimizations
- **[Optimize Infrastructure](optimize-infrastructure.md)**: Optimize infrastructure performance

### Performance
- **[Optimize Performance SEO](../growth/optimize-performance-seo.md)**: Optimize performance for SEO
- **[Check System Health](check-system-health.md)**: Check overall system health

### Guidelines
- **[Performance Optimization](.cursor/rules/performance-optimization.mdc)**: Performance best practices
- **[Next.js Performance](https://nextjs.org/docs/app/building-your-application/optimizing)**: Next.js optimization features


# Monolithic Wordpress

### Woocommerce

- Create a plugin to add products (i.e., Missionaries & Projects) in WooCommerce programmatically
- Create a hook or Chron Job to create, update, or destroy products, sourced via informatica
- Custom code - [this article](https://quadlayers.com/add-products-woocommerce/) & [this one](https://devnetwork.io/add-woocommerce-product-programmatically/)
- Integration to Worldpay (Hosted Payment page) costs \$79/yr with 1 year of updates and support
  - Custom hosted payment response handling ([save successfull payment/cart to DB/Informatica](https://docs.woocommerce.com/document/payment-gateway-api/))

### Wycliffe Custom Theme?

- If yes
  - Build on Tailwind CSS
  - Custom [reusable] Components
  - Templating more difficult
- If no
  - Divi, Elementor, Etc.? (i.e., visual editors)
  - Concern for landing pages/customization
  - Components based Dev
    - e.g., [https://flyntwp.com/](https://flyntwp.com/)
      - [Set-up](https://flyntwp.com/the-beginners-guide-to-developing-a-custom-wordpress-theme-with-flynt/)
- Initial Recommendation ->
  - No. Use Divi, one-time paid @\$200-something, which has [decent documentation](https://www.elegantthemes.com/documentation/developers/) for many customizaitons, including developing custom "modules"
    - Find a Base Theme
    - Module, Theme, and Templating development (HTML, PHP, JS, React, CSS)
      - Recommendation: Do not have contractors build custom theming (provide and roll-out in-house changes)
    - Unsettled:
      - How will we import existing blogs, missionaries, etc, to [custom] Divi templates?
        - Articles
        - [https://clicknathan.com/web-design/automatically-create-pages-wordpress/](https://clicknathan.com/web-design/automatically-create-pages-wordpress/)
        - [https://blog.wplauncher.com/add-wordpress-post-or-page-programmatically/](https://blog.wplauncher.com/add-wordpress-post-or-page-programmatically/)
        - [https://yoohooplugins.com/create-wordpress-post-page-php/](https://yoohooplugins.com/create-wordpress-post-page-php/)

### Plugins

- Custom fetchers (Missionary, Projects, etc.)
- Custom integration for User Data
  - Workday REST integration for Wordpress, e.g. -> [here](https://www.workato.com/integrations/wordpress+workday_rest)
  - Login/Profile [plugins](https://www.cozmoslabs.com/154636-best-wordpress-user-profile-plugins-compared/) need customization via Informatica data (existing users/missionaries/gifts)
    - Tied to Bookmarking (Custom plugin)
    - Image Uploading to modify Workday data (Custom plugin)
- Integrates with Sendgrid, Pardot

### Static Sites

- Can [host static sites](https://www.templatemonster.com/blog/integrate-static-html-wordpress/) from WebRoot for Custom Landing Pages

### Hosting

- Pantheon?
- Github Code

##### Reverse Proxying

To clarify, by reverse proxy I’ve meant that we have the ability to choose certain URLs, for example “wycliffe.org/donate”, which will on a brand-new site, actually reflect the contents and functionality of the old-site. In this way we would migrate more slowly to a new platform.

Per Dave,

> We may be able to [reverse proxy the old website pages] at [the application gateway](https://docs.microsoft.com/en-us/azure/application-gateway/create-url-route-portal)

Nevertheless, this "if" is important for moving forward and rolling out a development plan.

### Content-Creator Experience

The Wordpress platform is far superior in user-friendliness, and insofar as we want non-developers (not familiar with basic HTML, CSS, JS) interacting with the site, this has far more potential for ease of access.

For the Developer, however, it is far more inaccessible and will cause slower experiences. For some pages, which require fast rolling-out, it is possible, though not necessarily recommended, to host static pages.

### Workflow / Dev-Environment

- Articles
  - [https://premium.wpmudev.org/blog/improve-wordpress-development-workflow-local-server/](https://premium.wpmudev.org/blog/improve-wordpress-development-workflow-local-server/)
  - [https://css-tricks.com/continuous-deployments-for-wordpress-using-github-actions/](https://css-tricks.com/continuous-deployments-for-wordpress-using-github-actions/)
- Local
  - [https://localwp.com/](https://localwp.com/)

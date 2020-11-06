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
- Recommendation ->
  - No. Use Divi, one-time paid @\$200-something, which has [decent documentation](https://www.elegantthemes.com/documentation/developers/) for many customizaitons, including developing custom "modules"
    - Find a Base Theme
    - Module, Theme, and Templating development (HTML, PHP, JS, React, CSS)
      - Recommendation: Do not have contractors build custom theming (provide and roll-out in-house changes)
    - Unsettled:
      - How will we import existing blogs, missionaries, etc, to [custom] Divi templates?

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

### Workflow / Dev-Environment

<!--Todo-->

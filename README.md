# Custom Age Verifier and Tax Plugin

A custom WordPress plugin to add an age verifier and apply taxes to specific product categories for WooCommerce.

## Features

- **Age Verification**: Popup modal requiring users to verify they are 19+ years old before accessing the site
- **Province-based Tax Calculation**: Automatically applies Canadian provincial tax rates based on user location
- **Product Category Tax Control**: Configure which product categories are subject to taxation
- **Province-specific Product Hiding**: Hide specific products or categories from certain provinces
- **WooCommerce Integration**: Seamlessly integrates with WooCommerce checkout and cart functionality
- **Responsive Design**: Mobile-friendly age verification popup

## Installation

1. Upload the plugin files to the `/wp-content/plugins/custom-age-verifier-tax` directory
2. Activate the plugin through the 'Plugins' screen in WordPress
3. Configure the plugin settings in WooCommerce > Settings > Age Verifier & Tax

## Requirements

- WordPress 5.0 or higher
- WooCommerce 3.0 or higher
- PHP 7.4 or higher

## Configuration

### Age Verification
- Customizable age limit (default: 19 years)
- Province selection dropdown
- Birth date verification
- Cookie-based session management

### Tax Settings
Configure tax rates for each Canadian province:
- Alberta (AB): 5%
- British Columbia (BC): 12%
- Manitoba (MB): 12%
- New Brunswick (NB): 15%
- Newfoundland and Labrador (NL): 15%
- Nova Scotia (NS): 15%
- Ontario (ON): 13%
- Prince Edward Island (PE): 15%
- Quebec (QC): 14.975%
- Saskatchewan (SK): 11%
- Northwest Territories (NT): 5%
- Nunavut (NU): 5%
- Yukon Territory (YT): 5%

### Product Management
- Select taxable product categories
- Configure province-specific product hiding
- Set special tax rates for specific product sizes (60ml, 120ml)

## File Structure

```
custom-age-verifier-tax/
├── woo-price-calc.php          # Main plugin file
├── js/
│   ├── age-verifier.js         # Age verification functionality
│   ├── d-admin.js              # Admin interface scripts
│   └── woocommerce-address-handler.js  # Address handling
├── WC_Settings_Custom.php      # Custom WooCommerce settings
├── styles.css                  # Plugin styles
└── README.md                   # This file
```

## Usage

1. **Age Verification**: Users will see a popup on first visit requiring age verification
2. **Province Selection**: Users select their province for tax calculation
3. **Tax Application**: Taxes are automatically calculated and displayed on product pages
4. **Checkout Integration**: Province information is automatically applied to checkout forms

## Customization

The plugin provides several hooks and filters for customization:

- `woocommerce_get_price_html` - Modify price display
- `woocommerce_checkout_fields` - Customize checkout fields
- `woocommerce_is_purchasable` - Control product purchasability

## Support

For support and feature requests, please contact [Block Agency](https://blockagency.co).

## License

This plugin is proprietary software developed by Block Agency.

## Version

Current version: 1.0

## Changelog

### Version 1.0
- Initial release
- Age verification functionality
- Province-based tax calculation
- Product category tax control
- Province-specific product hiding

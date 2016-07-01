# Debug
[![License](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
![Downloads](https://img.shields.io/packagist/dt/wpbp/cpt_columns.svg) 

Improve the CPT list in the backend for your CPTs

## Install

`composer require wpbp/cpt_columns:dev-master`

[composer-php52](https://github.com/composer-php52/composer-php52) supported.

## Example

```php
$post_columns = new CPT_columns( 'demo' );
$post_columns->add_column( 'cmb2_field', array(
    'label' => __( 'CMB2 Field' ),
    'type' => 'post_meta', //text, thumbnail, post_meta, author, custom_tax, custom_value
    'meta_key' => '_demo_meta_text',
    'orderby' => 'meta_value', // For WP-Query
    'sortable' => true,
    'prefix' => '<b>',
    'suffix' => '</b>',
    'def' => 'Not defined', // Default value in case post meta not found
    'order' => '-1' // This is the last column
	)
);
```

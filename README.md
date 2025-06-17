# Icon Action Toolbar

[![Latest Version on Packagist](https://img.shields.io/packagist/v/mlsolutions/icon-action-toolbar)](https://packagist.org/packages/mlsolutions/icon-action-toolbar)
[![Total Downloads](https://img.shields.io/packagist/dt/mlsolutions/icon-action-toolbar)](https://packagist.org/packages/mlsolutions/icon-action-toolbar)
[![License](https://img.shields.io/packagist/l/mlsolutions/icon-action-toolbar)](https://github.com/ml-solutions-ltda/icon-action-toolbar/blob/master/LICENSE)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ml-solutions-ltda/icon-action-toolbar/main/screenshots/dark.png">
  <img alt="Icon Action Toolbar in Action" src="https://raw.githubusercontent.com/ml-solutions-ltda/icon-action-toolbar/main/screenshots/light.png">
</picture>

Replaces the default boring action menu with an inline row of icon-based actions. 

# Installation

You can install the package via composer:

```
composer require mlsolutions/icon-action-toolbar
```

## Basic Usage

All you need to do is append an `->icon()` to all your actions, it accepts either an icon name from [heroicons](https://heroicons.com/) or inlined svg string.

```php
class UserResource extends Resource
{
    public function actions(NovaRequest $request): array
    {
        return [
            UpdateSubscription::make()->icon('credit-card'),
            Unban::make()->icon('fire'),
            
            DeleteInactiveUsers::make()->standalone()->icon('hand', label: 'Ban!'),
            SendWeekNewsletter::make()->standalone()->icon('<svg>...</svg>'),
        ];
    }
}
```

## Configuration

You can customize the icons by adding the following to your nova config file:

```php
// config/nova.php

'vendors' => [
    'icon_action_toolbar' => [
        'icons' => [
            'replicate' => 'square-2-stack',
            'preview' => 'viewfinder-circle',
            'impersonate' => 'finger-print',
            'delete_resource' => '<svg>...</svg>',
        ],
    ]
]
```

## ⭐️ Show Your Support

Please give a ⭐️ if this project helped you!

### Other Packages You Might Like

- [Nova Dashboard](https://github.com/ml-solutions-ltda/nova-dashboard) - The missing dashboard for Laravel Nova!
- [Nova Welcome Card](https://github.com/ml-solutions-ltda/nova-welcome-card) - A configurable version of the `Help card` that comes with Nova.
- [Icon Action Toolbar](https://github.com/ml-solutions-ltda/icon-action-toolbar) - Replaces the default boring action menu with an inline row of icon-based actions.
- [Expandable Table Row](https://github.com/ml-solutions-ltda/expandable-table-row) - Provides an easy way to append extra data to each row of your resource tables.
- [Collapsible Resource Manager](https://github.com/ml-solutions-ltda/collapsible-resource-manager) - Provides an easy way to order and group your resources on the sidebar.
- [Resource Navigation Tab](https://github.com/ml-solutions-ltda/resource-navigation-tab) - Organize your resource fields into tabs.
- [Resource Navigation Link](https://github.com/ml-solutions-ltda/resource-navigation-link) - Create links to internal or external resources.
- [Nova Mega Filter](https://github.com/ml-solutions-ltda/nova-mega-filter) - Display all your filters in a card instead of a tiny dropdown!
- [Nova Pill Filter](https://github.com/ml-solutions-ltda/nova-pill-filter) - A Laravel Nova filter that renders into clickable pills.
- [Nova Slider Filter](https://github.com/ml-solutions-ltda/nova-slider-filter) - A Laravel Nova filter for picking range between a min/max value.
- [Nova Range Input Filter](https://github.com/ml-solutions-ltda/nova-range-input-filter) - A Laravel Nova range input filter.
- [Nova FilePond](https://github.com/ml-solutions-ltda/nova-filepond) - A Nova field for uploading File, Image and Video using Filepond.
- [Custom Relationship Field](https://github.com/ml-solutions-ltda/custom-relationship-field) - Emulate HasMany relationship without having a real relationship set between resources.
- [Column Toggler](https://github.com/ml-solutions-ltda/column-toggler) - A Laravel Nova package that allows you to hide/show columns in the index view.
- [Batch Edit Toolbar](https://github.com/ml-solutions-ltda/batch-edit-toolbar) - Allows you to update a single column of a resource all at once directly from the index page.

## License

The MIT License (MIT). Please see [License File](https://raw.githubusercontent.com/ml-solutions-ltda/icon-action-toolbar/master/LICENSE) for more information.

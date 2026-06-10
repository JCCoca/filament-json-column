# filament-json-column

V1 of the package, built for Filament 5.

## Overview

`filament-json-column` provides a compact JSON viewer and editor for Filament 5 forms and infolists. It is intended for JSON or array cast attributes in your Eloquent models.

## Installation

```bash
composer require jccoca/filament-json-column
```

## Usage

Add the component to a Filament 5 schema.

```php
use Filament\Schemas\Schema;
use JCCoca\FilamentJsonColumn\JsonColumn;
use JCCoca\FilamentJsonColumn\JsonInfolist;

public static function form(Schema $schema): Schema
{
    return $schema->schema([
        JsonColumn::make('example'),
    ]);
}

public static function infolist(Schema $schema): Schema
{
    return $schema->schema([
        JsonInfolist::make('example'),
    ]);
}
```

The form component provides both a viewer and an editor, with automatic JSON validation.

## Compatibility

- Filament 5.x
- PHP 8.2+
- Laravel 12.x

## Credits

Inspired by Pretty JSON and JSONeditor.
Original code base created by [valentin-morice](https://github.com/valentin-morice/).

This package loads JSONEditor from a CDN. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for third-party notices.

## License

The package code is released under the MIT License. See [LICENSE.md](LICENSE.md) for details.

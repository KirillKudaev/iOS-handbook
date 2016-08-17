# Project Structure

The physical files should be kept in sync with the Xcode project files in order to avoid file sprawl. Any Xcode groups created should be reflected by folders in the filesystem. Code should be grouped by type and feature for greater clarity.

Make sure to use an [app-template](https://github.com/bakkenbaeck/app-template) for consistency.

```
Project
|
|— Assets # Shared assets
|—— Fonts
|
|— Vendor # 3rd party code that doesn't use CocoaPods or Carthage
|—— METCalendarViewer
|—— LZOPhotoViewer
|
|— Library # Anything that falls outside of the MVC pattern or is shared between targets
|—— Extensions
|——— Theme.swift
|—— Fetchers
|——— Fetcher.swift
|——— RecipesFetcher.swift
|——— IngredientsFetcher.swift
|—— Subclasses
|—— BaseClasses
|—— Models
|——— Autogenerated # Generated by mogenerator
|———— _Recipe.swift
|———— _Ingredient.swift
|——— Recipe.swift
|——— Ingredient.swift
|——— DataModel.xcdatamodeld
|
|— iOS
|—— Resources
|
|—— Source
|——— Root
|———— AppDelegate.swift

|——— Recipes
|—–—— Controllers
|———— Views
|
|—— Ingredients
|——— Controllers
|——— Views
|
|— Tests
```
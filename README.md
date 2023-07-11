[![pub package](https://img.shields.io/pub/v/custom_accordion.svg)](https://pub.dartlang.org/packages/custom_accordion) [![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=102)](https://opensource.org/licenses/MIT) [![License](https://img.shields.io/badge/license-MIT-orange.svg)](https://github.com/zeeshanayaz/custom_accordion/blob/master/LICENSE) 

# Custom Accordion

Custom Accordion (Expandable) widget with lots of customization.

## Table of contents 
- [Demo Preview](#demo-preview)
- [Get Started](#get-started)
- [How to use](#how-to-use)
- [Properties](#properties)
- [Contributing](#contributing)


## Demo Preview

<img src="https://github.com/zeeshanayaz/custom_accordion/raw/master/demo/custom_accordion_example.gif" height="600" />

## Get Started

### Add to your project
```
flutter pub add custom_accordion
```

### Import and use it!
```
import 'package:custom_accordion/custom_accordion.dart';
```

## How to use

Basic Accordion
```dart
    CustomAccordion(
        title: 'Accordion',
        ),
```

Accordion with no child
```dart
    CustomAccordion(
        title: 'Accordion with no child',
        subTitle: 'Accordion Sub Title',
        headerBackgroundColor: Colors.blue,
        titleStyle: const TextStyle(
          fontSize: 18,
          fontWeight: FontWeight.bold,
          color: Colors.white,
        ),
        subTitleStyle: const TextStyle(
          fontSize: 16,
          fontWeight: FontWeight.normal,
          color: Colors.white,
        ),
        toggleIconOpen: Icons.keyboard_arrow_down_sharp,
        toggleIconClose: Icons.keyboard_arrow_up_sharp,
        headerIconColor: Colors.white,
        accordionElevation: 0,
        showContent: true,
        ),
```

Accordion with one child
```dart
    CustomAccordion(
        title: 'Accordion with one child',
        subTitle: 'Accordion Sub Title',
        headerBackgroundColor: Colors.blue,
        titleStyle: const TextStyle(
          fontSize: 18,
          fontWeight: FontWeight.bold,
          color: Colors.white,
        ),
          subTitleStyle: const TextStyle(
          fontSize: 16,
          fontWeight: FontWeight.normal,
          color: Colors.white,
        ),
        toggleIconOpen: Icons.keyboard_arrow_down_sharp,
        toggleIconClose: Icons.keyboard_arrow_up_sharp,
        headerIconColor: Colors.white,
        accordionElevation: 0,
        widgetItems: const Text(
          'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.',
          ),
        ),
```
Accordion with many child
```dart
    CustomAccordion(
        title: 'Accordion with many child',
        headerBackgroundColor: Colors.blue,
        titleStyle: const TextStyle(
          fontSize: 18,
          fontWeight: FontWeight.bold,
          color: Colors.white,
        ),
        toggleIconOpen: Icons.keyboard_arrow_down_sharp,
        toggleIconClose: Icons.keyboard_arrow_up_sharp,
        headerIconColor: Colors.white,
        accordionElevation: 0,
        widgetItems: Column(
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: [
              Text(
                'Lorem Ipsum',
                style: Theme.of(context).textTheme.titleMedium,
              ),
              ElevatedButton(
                onPressed: () {},
                child: const Text(
                  'ELEVATED BUTTON',
                ),
              )
            ],
          ),
        ),
```

Accordion with List Items and disabled toggle example
```dart
        CustomAccordion(
            title: 'Accordion with List Items',
            subTitle: 'Accordion toggle disabled',
            headerBackgroundColor: Colors.blue,
            titleStyle: const TextStyle(
              fontSize: 18,
              fontWeight: FontWeight.bold,
              color: Colors.white,
            ),
            subTitleStyle: const TextStyle(
              fontSize: 16,
              fontWeight: FontWeight.normal,
              color: Colors.white,
            ),
            toggleIconOpen: Icons.keyboard_arrow_down_sharp,
            toggleIconClose: Icons.keyboard_arrow_up_sharp,
            headerIconColor: Colors.white,
            accordionElevation: 0,
            disableToggle: true,
            widgetItems: Column(
                crossAxisAlignment: CrossAxisAlignment.stretch,
                children: List<Widget>.generate(5, (int index) {
                return Text('Item $index');
                }),
            ),
        ),
```

Please see example project for code.


## Properties

The following properties can be set for the widget.

| Property              | Description                                                     | Type               | Required | Default value                          |
|-----------------------|-----------------------------------------------------------------|--------------------|----------|----------------------------------------|
| title                 | Title of Accordion                                              | String             | Yes      |                                        |
| subTitle              | Sub Title of Accordion                                          | String             | No       |                                        |
| headerBackgroundColor | Header background color                                         | Color              | No       | Theme.of(context).splashColor          |
| titleStyle            | Header text style                                               | TextStyle          | No       | Theme.of(context).textTheme.titleLarge |
| subTitleStyle         | Sub Title text style                                            | TextStyle          | No       | Theme.of(context).textTheme.titleSmall |
| toggleIconOpen        | Toggle icon to expand/open widgets                              | IconData           | No       | Icons.arrow_drop_down                  |
| toggleIconClose       | Toggle icon to collapse/close widgets                           | IconData           | No       | Icons.arrow_drop_up                    |
| headerIconColor       | Icon Color                                                      | Color              | No       | Theme.of(context).iconTheme.color      |
| backgroundColor       | Background color of widget                                      | Color              | No       | Theme.of(context).cardColor            |
| accordionElevation    | Elevation of accordion widget                                   | double             | No       | Theme.of(context).cardTheme.elevation  |
| widgetItems           | Child Widget(s) of accordion                                    | Widget             | No       | Text()                                 |
| widgetItemsPadding    | Padding arround children of accordion                           | EdgeInsetsGeometry | No       | EdgeInsets.all(10)                     |
| showContent           | Make default behaviour of accordion children visible or hidden  | bool               | No       | false                                  |
| disableToggle         | Make default behaviour of accordion toggle                      | bool               | No       | false                                  |


## Contributing

Custom Accordion is **100% free** and **open source**. We encourage and support an active, healthy community that accepts contributions from the public &ndash; including you. There are a couple of ways in which you can contribute.

  * Fix a bug
  * Write and improve some **documentation**. Documentation is very critical to us. We would appreciate help in adding multiple languages to our docs.
  * If you are a developer, feel free to check out the source and submit pull requests.
  * Dig into [**CONTRIBUTING.MD**](CONTRIBUTING.md), which covers submitting bugs, requesting new features, preparing your code for a pull request, etc.
  * Please don't forget to **like**, **follow**, and **star our repo**!.

# MDX Components Documentation

This documentation covers the available MDX components for rendering dynamic content.

## Table of Contents

- [TabGroup & Tab](#tabs)
- [Featured Checklist](#FeaturedChecklist)
- [List](#list)
- [Feature With Image](#featurewithimage)
- [Places](#places)
- [Long Content](#LongContent)

## Usefull links

- <a href="https://lucide.dev/icons" target="_blank">Lucid icons</a>

## Components

### Tabs

Creates an interactive tabbed interface with optional auto-switching functionality.

#### TabGroup Props
- `title` (string) - Main heading for the tab group
- `subtitle` (string) - Descriptive text below the title
- `duration` (number) - Time in seconds before switching to next tab automatically
- `background` (boolean) - Enables dark background mode

#### Tab Props
- `name` (string, required) - Tab label
- `icon` (string) - Lucide icon name
- `imageUrl` (string) - URL for tab's image

```jsx
<TabGroup title="Our Services" subtitle="Explore what we offer" duration={5} background={false}>
    <Tab name="Design" icon="Palette" imageUrl="/images/design.jpg">
        ## Design Services
        Professional design services tailored to your needs.
    </Tab>
</TabGroup>
```
------

### FeaturedChecklist

Creates a checklist with optional image, title, and call-to-action.

#### Props
- `imageUrl` (string) - Featured image URL
- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `cta` (string) - Call-to-action button text
- `link` (string) - CTA button destination URL (required if `cta` is set)
- `cols` (number, 1-4) - Number of columns for checklist items
- `theme` (string) - Visual theme ('dark' | 'light')
- `ctaPlacement` (string) - CTA button position ('left' | 'center' | 'right')
- `checkIcon` (string) - Default Lucide icon name for list items

```jsx
<FeaturedChecklist imageUrl="/image.jpg" title="Features" subtitle="Key benefits" cta="Learn More" link="/features" cols={2} theme="dark">
    * [CheckCircle] Feature 1
    * Feature 2
</FeaturedChecklist>
```

------

### List

Creates a structured list with optional icons and descriptions.

#### Props
- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `direction` (string) - Layout direction ('vertical' | 'horizontal')
- `cols` (number, 1-5) - Number of columns
- `hasIcon` (boolean) - Show/hide icons
- `checkIcon` (string) - Default Lucide icon name

```jsx
<List title="Process" subtitle="Our workflow" direction="vertical" cols={2}hasIcon={true}checkIcon="Check">
    * [Heart] Planning: Initial planning phase

    * Implementation: Execution phase
</List>
```
#### Notes
- keep a new empty line between list items
- use `[ ]` to add an icon to a list item

------

### FeatureWithImage

Displays a feature section with image and descriptive content.

#### Props
- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `imageUrl` (string) - Feature image URL
- `theme` (string) - Color theme ('dark' | 'light')
- `className` (string) - Additional CSS classes

```jsx
<FeatureWithImage title="Key Feature" subtitle="Description" imageUrl="/feature.jpg" theme="dark">
    * [Utensils] Feature 1: Detailed description
    
    * Feature 2: Another description
</FeatureWithImage>
```

#### Notes
- keep a new empty line between list items
- use `[ ]` to add an icon to a list item

------

### Places

Creates a grid layout of places/locations with featured items.

#### Places Props
- `title` (string) - Section title
- `subtitle` (string) - Section subtitle

#### FeaturedPlace Props
- `title` (string) - Place title
- `subtitle` (string) - Place description
- `imageUrl` (string) - Place image URL
- `url` (string) - Link destination

```jsx
<Places title="Destinations" subtitle="Popular locations">
    <FeaturedPlace title="Paris"subtitle="City of Light" imageUrl="/paris.jpg" url="/destinations/paris" />
    * [/london]London
    * [/rome]Rome
</Places>
```
------

## LongContent

Creates a two-column layout with left side content (70%) and right side image (30%). Perfect for long-form content like articles or detailed descriptions.

### Props

- `title` (string) - Main heading for the content section
- `subtitle` (string) - Descriptive text below the title
- `imageUrl` (string) - URL for the featured image
- `imageAlt` (string) - Alt text for the image
  
### Example

```jsx

<LongContent
    title="On a mission to empower remote teams"
    subtitle="Building better collaboration tools for the modern workplace"
    imageUrl="/images/team-collaboration.jpg"
    imageAlt="Team members collaborating remotely"
>
    ## Our Vision
    
    We believe in creating tools that make remote work more effective and enjoyable. 
    Our platform is designed to break down barriers and foster collaboration across 
    time zones and geographical boundaries.

    ### Key Benefits

    Remote work shouldn't mean disconnected work. Our tools bridge the gap between 
    team members, creating a seamless experience that rivals in-person collaboration.

    Through careful attention to user experience and performance, we've created a 
    platform that feels natural and intuitive, while providing powerful features 
    that remote teams need to succeed.
</LongContent>

```

------

### Best Practices

- Keep content width reasonable for readability
- Use Markdown headings for content structure
- Provide high-quality images that complement the content
- Use descriptive alt text for accessibility
- Ensure image aspect ratio works well with the fixed height container

## Icon Usage
- Components support [Lucide icons](https://lucide.dev/icons)
- Use icon names in square brackets: `[IconName]`
- Icons can be specified for individual list items or as default props

## Best Practices
- Use descriptive titles and subtitles
- Maintain consistent formatting in lists
- you can use either slug or full url for `imageUrl` prop
- in mobile all lists will be displayed in a single column
- use path for `url` prop (e.g: `/destinations/marrakech`)

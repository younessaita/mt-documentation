# MDX Components Documentation

This documentation covers the available MDX components and their usage. These components can be used directly in your MDX content.

## Table of Contents

- [Tab Group & Tabs](#tab-group--tabs)
- [Photo Checklist](#photo-checklist)
- [List](#list)
- [Feature With Icon](#feature-with-icon)

## Tab Group & Tabs

Creates an interactive tabbed interface with optional auto-switching functionality.

### Props

#### TabGroup

- `title` (string) - Main heading for the tab group
- `subtitle` (string) - Descriptive text below the title
- `duration` (number) - Time in seconds before switching to next tab automatically
- `background` (boolean) - Enable dark background mode

#### Tab

- `name` (string, required) - Tab label
- `icon` (string) - Lucide icon name
- `imageUrl` (string) - URL for tab's image

### Example

```jsx
<TabGroup title="Our Services" subtitle="Explore what we offer" duration={5}>
    <Tab name="Design" icon="Palette" imageUrl="/images/showcase.jpg">
        ## H2 Heading Professional interior design services tailored to your needs.
    </Tab>
    <Tab name="Consultation" icon="MessageCircle">
        Expert consultation to bring your vision to life.
    </Tab>
</TabGroup>
```

### Best Practices

- Keep tab names concise
- Use relevant icons to enhance visual hierarchy
- Provide meaningful content within each tab
- Don't use (`duration`) prop so tabs won't switch automatically

## Featured Checklist

Creates a visually appealing checklist with an optional image.

### Props

- `imageUrl` (string) - URL of the featured image
- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `cta` (string) - Call-to-action button text
- `ctaPlacement` (string) - Call-to-action button placement (left | center | right, default: left)
- `link` (string) - CTA button destination URL
- `cols` (number) - Number of columns (1-4, default: 2)
- `background` (boolean) - Enable/disable background styling
### Example

```jsx
<FeaturedChecklist imageUrl="/images/interior.jpg" title="Design Process" subtitle="Our comprehensive approach" cta="Start Your Project" link="/contact" cols={2}>
    * Initial Consultation * Design Concept * Material Selection * Implementation
</FeaturedChecklist>
```

## List

Creates a structured list with titles and descriptions.

### Props

- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `direction` ("vertical" | "horizontal", default: "vertical") - Layout direction
- `cols` (number, 1-5, default: 2) - Number of columns

### Example

```jsx
<List title="Our Process" subtitle="How we work with clients" direction="vertical" cols={2}>
    * Initial Meeting: We discuss your vision and requirements. 
    * Design Phase: Creating detailed plans and mockups. 
    * Implementation: Bringing designs to life with precision.
</List>
```

### List format

- Each item must follow the format: `* Title: Description`
- Use a colon to separate title from description
- One item per line
- Leave a blank line before and after the list

## Feature With Icon

Creates a feature section with icons and descriptions.

### Props

- `title` (string) - Main heading
- `subtitle` (string) - Supporting text
- `image` (string) - URL of the feature image
- `theme` ("light" | "dark") - Color theme
- `background` (boolean) - Enable/disable background styling

### Example

```jsx
<FeatureWithIcon title="Our Expertise" subtitle="What sets us apart" image="/images/showcase.jpg" theme="light">
    * [Brush] Design Excellence: Creating stunning spaces that inspire 
    * [Shield] Quality Assurance: Premium materials and craftsmanship 
    * [Clock] Timely Delivery: Meeting deadlines with precision
</FeatureWithIcon>
```

### List Format

- Each item must follow the format: `* [IconName]Title: Description`
- Icon name must be a valid Lucide icon name in square brackets
- Use a colon to separate title from description
- One item per line
- Leave a blank line before and after the list

### Best Practices

- Choose relevant icons that complement the content
- Keep titles concise and descriptive
- Provide detailed descriptions
- Maintain consistent formatting across items

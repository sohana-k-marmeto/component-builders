# Design System for Hypothetical Company Dashboard

This design system provides a set of reusable, scalable, and accessible components to help you build faster and design smarter. The components in this system include Buttons, Cards, and Inputs, all with a focus on a visually appealing and user-friendly interface.

## Objective
The goal of this project is to create a simple, reusable design system that can be integrated into various dashboards or web applications. The system follows best practices for accessibility and responsiveness, ensuring a seamless user experience across devices.

## Getting Started

To start using the components, you can open the `index.html` file in your browser. It will link you to each component's page where you can explore individual usage and styling guidelines. All the base CSS for elements like wrappers,root variables are written in `style.css` and the component specific CSS is written in the respective CSS files.

## Folder Structure

```
├── index.html
├── style.css
├── button-component
   ├── button.html
   ├── button.css
├── card-component
   ├── card.html
   ├── card.css
├── input-component
   ├── input.html
   ├── input.css

```
## Components

# Button Component

## Overview
The Button Component is a reusable design element with multiple styles and sizes to suit a variety of use cases. It supports primary, secondary, gradient, outlined, and disabled states, offering flexibility in UI design.

---

## API/Props

### Classes
Below are the available classes to customize buttons:

| Class Name       | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `btn`            | Base class for all buttons.                                                |
| `btn-primary`    | Applies the primary button style (solid background).                      |
| `btn-secondary`  | Applies the secondary button style (outlined border).                     |
| `btn-small`      | Sets the button size to small.                                             |
| `btn-medium`     | Sets the button size to medium (default size).                             |
| `btn-large`      | Sets the button size to large.                                             |
| `btn-rounded`    | Adds rounded corners to the button.                                        |
| `btn-gradient`   | Adds a gradient background or border (depending on `btn-primary` or `btn-secondary`). |
| `[disabled]`     | Disables the button and changes its appearance to indicate unavailability. |

---

## Styling Considerations

### CSS Variables
To customize the component, define the following CSS variables in your stylesheet:
- `--primary-color`: Sets the primary color of buttons.
- `--primary-color-gradient`: Sets the secondary color for gradient buttons.
- `--font-size-small`, `--font-size-medium`, `--font-size-large`: Control the font sizes for different button sizes.
- `--padding-small`, `--padding-medium`, `--padding-large`: Control the padding for different button sizes.
- `--border-radius`: Sets the border-radius for rounded buttons.

### Fonts
This component uses the [Inter font](https://fonts.google.com/specimen/Inter). Ensure it is included in your project:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet">
```
## Styling Considerations
1. **Font**: All buttons use the 'Inter' font-family for consistent typography.
2. **Responsiveness**: Button sizes adjust based on screen size, making them suitable for various device widths.
3. **Colors**: Button colors are controlled using CSS variables (`--primary-color`, `--primary-color-gradient`, `--font-size-small`, etc.). Ensure these variables are defined for consistent styling.
4. **Accessibility**: Buttons are designed with proper focus states and `aria-disabled` attributes for better accessibility.

## Examples of Usage

### 1. Primary Solid Button (Small)
```html
<button class="btn btn-primary btn-small  btn-rounded">Button</button>
```
# Card Component

## Overview
The `Card Component` is a reusable design element designed for flexibility and ease of use. It supports various configurations, including cards with images, buttons, and links, as well as cards without actions or images.

## File Structure
- **HTML**: Contains the structure for different types of card components.
- **CSS**: Styling rules for the card components, including reusable utility classes for buttons and layout.

---

## API/Props

### Card Component
| Prop          | Type    | Description                                                                                 | Default             |
|---------------|---------|---------------------------------------------------------------------------------------------|---------------------|
| `card-title`  | String  | The main heading text for the card.                                                         | N/A                 |
| `card-subtitle` | String | A subtitle text for additional context.                                                    | N/A                 |
| `card-description` | String | A detailed description for the card content.                                             | N/A                 |
| `card-image`  | String (URL) | URL for the image displayed at the top of the card.                                       | No image by default |
| `card-action` | Element | A button or link element for card actions.                                                  | Optional            |

### Button Props
| Prop             | Type    | Description                                                                              | Default             |
|-------------------|---------|------------------------------------------------------------------------------------------|---------------------|
| `button-primary`  | Class   | Styles the button with the primary color scheme.                                         | N/A                 |
| `button-link`     | Class   | Styles the button as a text link.                                                        | N/A                 |

---

## Styling Considerations
1. **CSS Variables**:
   - Ensure the following CSS variables are defined in your global stylesheet:
     - `--border-radius`
     - `--padding-small`
     - `--padding-medium`
     - `--primary-color`
     - `--secondary-color`
     - `--font-size-small`
     - `--font-size-medium`
     - `--transition`

2. **Flexibility**:
   - The card layout supports a flexible height and automatically adjusts content alignment.

3. **Hover Effects**:
   - Cards include a hover effect that slightly lifts the card (`transform: translateY(-5px);`).

---

## Examples of Usage

### Card with Button
```html
<div class="card">
  <img src="example-image.jpg" alt="Card Image" class="card-image">
  <div class="card-content">
    <h3 class="card-title">Card Title</h3>
    <p class="card-subtitle">Card Subtitle</p>
    <p class="card-description">This is a description of the card content.</p>
  </div>
  <button class="button button-primary card-action">Click Me</button>
</div>
```
# Input Component

## Overview
The `Input Component` is a reusable form element designed for accessibility and visual consistency. It includes support for various states such as normal, focused, error, and disabled, with appropriate styles for each state.

## File Structure
- **HTML**: Provides the structure for input fields with different states.
- **CSS**: Contains styles for the input fields, error messages, and their responsive interactions.

---

## API/Props

### Input Component
| Prop             | Type      | Description                                                                    | Default Value         |
|-------------------|-----------|--------------------------------------------------------------------------------|-----------------------|
| `id`             | String    | Unique identifier for the input field.                                         | Required              |
| `class`          | String    | CSS class applied to the input field to define its state or style.             | `input-field`         |
| `placeholder`    | String    | Text displayed inside the input field when it is empty.                        | N/A                   |
| `value`          | String    | The initial value of the input field.                                          | Empty string          |
| `disabled`       | Boolean   | Disables the input field, making it non-interactive.                           | `false`               |
| `error-message`  | String    | The error message displayed when the input field is in the error state.        | Empty string          |

---

## Styling Considerations

1. **CSS Variables**:
   - Ensure the following variables are defined in your global stylesheet for consistent theming:
     - `--border-color`
     - `--text-color`
     - `--primary-color`
     - `--error-color`
     - `--error-bg`
     - `--disabled-color`
     - `--secondary-color`
     - `--border-radius`
     - `--padding-medium`
     - `--font-size-small`
     - `--font-size-medium`
     - `--transition`

2. **Responsive Design**:
   - The input fields are designed to be fully responsive and adapt to container widths.

3. **Hover and Focus Effects**:
   - Focused fields have a border highlight and subtle box shadow for better visibility.

4. **Error Handling**:
   - Input fields in the error state have a distinct border and background color with an accompanying error message.

---

## Examples of Usage

### Normal State
```html
<div class="form-group">
  <label for="default">Normal</label>
  <input type="text" id="default" class="input-field" placeholder="Enter text...">
</div>
```

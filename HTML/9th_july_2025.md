# July 8, 2025  
## Work With Me Form — HTML & CSS Diary Entry

Today I completed building a "Work With Me" form using only HTML and CSS. This is a part of my personal portfolio project, and the goal was to practice how forms are created, structured, and styled in pure front-end development without any JavaScript or frameworks.

---

## What I Built

The form is designed to collect key information from someone who wants to work or collaborate with me. It includes the following fields:

- Full Name (text input)
- Email (email input)
- Phone Number (telephone input)
- Gender (radio buttons: Male, Female, Prefer not to say)
- Years of Experience (dropdown menu)
- Availability Status (text input)
- Tagline (text input)
- About (textarea)
- LinkedIn URL (URL input)
- GitHub URL (URL input)
- Resume URL (URL input)
- Personal Website (URL input)
- Upload Photo (file input)

The submit button is labeled **"Save Profile"**.

---

## Input Types and Attributes

All input elements use proper HTML5 input types such as:

- `type="text"` for general text fields like name, tagline, and availability
- `type="email"` for email validation
- `type="tel"` for phone number inputs
- `type="url"` for web links like LinkedIn, GitHub, resume, and website
- `type="file"` for uploading a profile picture
- `type="radio"` for gender selection

I also used important attributes such as:

- `required` on fields like Full Name to enforce form completion
- `placeholder` to guide the user on expected input
- `accept="image/png, image/jpeg, image/gif"` to restrict image file types in the file upload
- `id` and `name` on every input to associate labels properly and make the form ready for backend submission

---

## Layout and Structure

The form uses a clean layout built with HTML and styled using internal CSS only (written in a `<style>` block in the same HTML file).

Layout decisions:

- Used Flexbox to create a responsive two-column layout on larger screens
- On smaller screens, the layout collapses into a single column using media queries
- Fields are grouped using `<div>` containers with classes like `.form-group`, `.row`, and `.col-half`

---

## Styling Choices

I used basic CSS to keep the form professional and minimal. Some of the choices include:

- Consistent padding and margins for clean spacing
- `border-radius` for rounded corners on inputs and buttons
- A soft box-shadow for the form container to separate it visually from the background
- System default fonts for simplicity and readability
- A hover effect on the submit button to give visual feedback

No external CSS frameworks or libraries were used.

---

## Why I Used Radio Buttons Instead of Location

Originally, many forms ask for city or location, but I decided to replace that with gender options. I used radio buttons because they allow selecting one value from a fixed list. All gender options are grouped under the same `name` attribute so only one can be selected.

The gender options are:

- Male
- Female
- Prefer not to say

---

## Validation and Accessibility

I followed basic best practices for accessibility and validation:

- All input fields are connected to labels using the `for` attribute (linked to the `id`)
- Inputs use the correct types (`email`, `url`, `tel`) to benefit from built-in HTML5 validation
- Placeholder text is used where helpful to guide input format
- The `name` attribute is used for every field so that data can be submitted and received by a backend later
- Grouped form fields logically and clearly to improve the user experience

---

## Summary

This project helped me practice and understand:

- How to structure an HTML form properly
- The role of each input type and when to use it
- How to use basic HTML attributes like `required`, `name`, `id`, `placeholder`, and `accept`
- How to build a responsive form layout using CSS Flexbox and media queries
- How to style a form without using any external libraries or JavaScript

The form is currently static and not connected to a backend. In future iterations, I may connect it to a service or build a backend to handle submissions.


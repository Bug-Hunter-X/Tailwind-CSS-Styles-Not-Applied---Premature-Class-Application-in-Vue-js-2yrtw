# Tailwind CSS Styles Not Applied in Vue.js Component

This repository demonstrates a common issue encountered when using Tailwind CSS with Vue.js: styles not being applied due to applying classes before the component's template is rendered.

## Problem

The `bug.vue` file shows an example where a Tailwind CSS class (`text-white`) is assigned to a component's data property.  Because this happens before the component is rendered, Tailwind might not correctly apply the class, resulting in missing or unexpected styles.

## Solution

The `bugSolution.vue` file illustrates the solution. The Tailwind class is applied directly in the template, ensuring that the class is applied after the component is rendered.  This ensures that Tailwind has the opportunity to apply the styles correctly.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run serve` (assuming you have a Vue CLI setup) to start the development server.
4. Observe that the original component in `bug.vue` doesn't have the expected styles, while the solution in `bugSolution.vue` does.
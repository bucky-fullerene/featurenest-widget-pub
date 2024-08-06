# Integrating FeatureNest Widget into Your Application 🕊️

Welcome to FeatureNest! Follow these simple steps to integrate the FeatureNest widget into your application. Let's get started!

## Step 1: Signup and Login
1. **Signup** on FeatureNest.
2. **Login** to your account.

## Step 2: Create a New Project
1. Click the **(+) button** on the lower right to create a new project.

## Step 3: Copy Your Project ID
1. Find your **project ID** on the dashboard.
2. **Copy** it for later use.

These initial steps remain the same irrespective of the tech stack you are using.

## HTML Integration 🌐

1. **Add the Script**: Insert the following script into the `<head>` of your HTML document:

    ```html
    <script src="https://cdn.jsdelivr.net/gh/bucky-fullerene/featurenest-widget-pub@non-prod/featurenest.js"></script>
    ```

2. **Hook the Project ID**: Add the `data-feature-nest-project-id` attribute to any button. For example:

    ```html
    <button data-feature-nest-project-id="66ae0e65971e5ed9bec9b7c8">Raise a FR</button>
    ```

   Replace `66ae0e65971e5ed9bec9b7c8` with your copied project ID.

## React.js Integration ⚛️

1. **Add the Script**: Use `useEffect` in the component where you want to integrate the widget:

    ```jsx
    import { useEffect } from 'react';

    useEffect(() => {
      const script = document.createElement('script');
      script.src = 'https://cdn.jsdelivr.net/gh/bucky-fullerene/featurenest-widget-pub@non-prod/featurenest.js';
      script.defer = true;
      document.body.appendChild(script);

      return () => {
        document.body.removeChild(script);
      };
    }, []);
    ```

2. **Hook the Project ID**: Add the `data-feature-nest-project-id` attribute to any button. For example:

    ```jsx
    <button data-feature-nest-project-id="66ae0e65971e5ed9bec9b7c8">Raise a FR</button>
    ```

   Replace `66ae0e65971e5ed9bec9b7c8` with your copied project ID.

That's it! 🎉 You have successfully integrated the FeatureNest widget into your application.

Happy feature nesting! 🚀. if you still run into nay issues hit me up on masakali@featurenest.co

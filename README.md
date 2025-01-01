# Next.js 15 App Router: Unexpected Behavior with Dynamic Routes and Data Fetching

This repository demonstrates an unexpected behavior in Next.js 15's App Router when combining dynamic routes and data fetching.  The issue is that data fetching sometimes does not occur correctly, leading to unexpected results or errors.

## Description

When using dynamic routes in the `app` directory and attempting to fetch data within the component, the data may not be correctly populated, even if the data fetching function completes successfully.

This is different from the Pages Router where data fetching would work reliably,  even with dynamic routes.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/post/[id]` with any valid id. 
5. Observe that data may be inconsistent or missing.

## Expected Behavior

The data fetched using `getServerSideProps` or a similar method should be consistently available within the component, regardless of the dynamic route parameters.

## Actual Behavior

Data fetching is unreliable in the `app` directory. Sometimes data is available, but other times it is not, even without changes to the code.

## Additional Context

This issue may be related to caching mechanisms or the way the App Router handles dynamic routes and data fetching.
# Space Launch Viewer

This project is an Angular application designed to display a list of space launches. It uses Apollo Client to interact with a GraphQL API to retrieve launch data.

## Features

- **Launch List**: Displays a list of space launches with details fetched from a GraphQL API.
- **Search Filter**: Allows users to filter launches by search text (not fully implemented in the code yet).
- **Loading State**: Shows a loading indicator while data is being fetched.
- **Error Handling**: Displays an error message if the data retrieval fails.

## Technologies Used

- **Angular**: A popular web application framework.
- **Apollo Client**: A GraphQL client used to query and manage application data.
- **GraphQL**: API technology used to retrieve data about space launches.
- **ChangeDetectionStrategy.OnPush**: Optimizes the performance by minimizing unnecessary change detection cycles in Angular.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/SeifeddineBS/space-launch-viewer.git
   cd space-launch-viewer
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Run the app:**

   ```bash
   ng serve
   ```

   The app should now be running at `http://localhost:4200/`.

## GraphQL API

The app retrieves space launch data through a GraphQL API. Ensure you have the correct API endpoint set up in your `graphql.queries.ts` file.

Example of a GraphQL query for fetching launches:

```typescript

   id
    mission_name
    links {
      flickr_images
      mission_patch_small
    }
    rocket {
      rocket_name
    }
    launch_date_utc
export const launches = gql`
  query GetLaunches {
    launches {
        id
        mission_name
        links {
            flickr_images
            mission_patch_small
        }
        rocket {
            rocket_name
        }
        launch_date_utc
  }
`;
```

## Future Enhancements

- **Search Functionality**: Implement search/filter logic to allow users to search launches by text (e.g., mission name).
- **Launch Details**: Display more detailed information for each launch.
- **Pagination**: Implement pagination or lazy loading to handle large datasets efficiently.

## License

This project is licensed under the MIT License.

---

### Screenshots

You can include screenshots or images of the app (once it’s fully functional) in this section.

This README outlines the project's purpose, its core features, and steps to set up and run the application. Let me know if you'd like to add or modify anything specific!
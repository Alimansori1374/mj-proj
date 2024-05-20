### Project Scope

At its core, this web application is dedicated to customs management, with a primary focus on import, export, and transit operations. As the project evolves, it is important to acknowledge that the system's capabilities may expand or be updated to accommodate changing requirements and regulations. Therefore, this documentation will remain a dynamic resource, reflecting the ongoing development and enhancements of the application.

In the upcoming sections, we will explore the different roles, features, and functionalities of this web application, providing you with a comprehensive understanding of how it can effectively support your customs (Gomrok) needs.

## Technical Stack

### Frontend - Sigma

1.  **React**: We chose React as the foundational JavaScript library for building the user interface. React's component-based architecture and virtual DOM make it a powerful tool for creating dynamic and interactive web applications.
2.  **Redux**: To manage the state of our application, we utilize Redux, a predictable state container. Redux helps us maintain a consistent and centralized state, ensuring that data flows smoothly through our application.
3.  **Redux Toolkit**: Redux Toolkit is employed to simplify the configuration and management of Redux in our project. It streamlines common Redux tasks, such as creating actions and reducers, making our codebase more maintainable and efficient.
4.  **RTK Query**: RTK Query is integrated to provide a robust data fetching and caching solution. It offers a convenient and efficient way to manage API requests and data updates in real-time, enhancing the performance and responsiveness of the application.

### Build Tools

In addition to the frontend technologies, we leverage a set of build tools to optimize the development and production workflows:

1.  **Vite**: Vite serves as our build tool and development server. It offers a fast and efficient development experience by utilizing native ES modules. Vite ensures quick startup times and efficient bundling, enhancing the overall development productivity.
2.  **OIDC (OpenID Connect)**: OIDC is utilized for authentication and identity management in our application. It enables secure user authentication and access control, ensuring that only authorized users can interact with the system.

### Package Management

All the required packages and dependencies for this project are listed in the `package.json` file. This file serves as a reference point for maintaining and managing the project's dependencies, ensuring version compatibility and stability.

In the following sections, we will dive deeper into the specific functionalities and components of our web application, providing you with a comprehensive understanding of how each aspect of the project works and interacts to deliver a seamless customs management experience.

To start this project on your local machine, follow these steps:

**Note:** Ensure you have the required permissions and administrative privileges to edit the host file.

1.  **Edit the Host File**:

    -   Open a text editor (e.g., Notepad) with administrative privileges. To do this, right-click on the text editor and choose "Run as administrator."
    -   Navigate to `C:\Windows\System32\drivers\etc` in the file dialog.
    -   Locate the file named `hosts` and open it.
    -   Add the domain addresses provided by your frontend team lead to this file. You can do this by adding entries in the following format:

        luaCopy code

        `127.0.0.1     example-domain-1.local 127.0.0.1     example-domain-2.local`

        Replace `example-domain-1.local` and `example-domain-2.local` with the actual domain addresses you received from your team lead.

    -   Save the `hosts` file and close the text editor.

2.  **Install Node Modules**:

    -   Open a command prompt or terminal window.
    -   Navigate to the project's root directory where the `package.json` file is located.
    -   Use one of the package managers (Yarn, npm, or pnpm) to install the project's related node modules. For example, if you're using Yarn, run:

        Copy code

        `yarn install`

        This command will fetch and install all the required dependencies specified in the `package.json` file.

3.  **Start the Project**:

    -   After the node modules are installed successfully, you can start the project. Depending on the configuration specified in your `package.json` file, you can use a command like:

        sqlCopy code

        `yarn start`

        This command will typically launch a development server and start the application on `localhost`. Follow any instructions provided by your project's documentation or frontend team lead regarding the specific command to start the project.

4.  **VPN**:

    -   Make sure any VPN software is turned off while running the project. VPNs can sometimes interfere with local development environments.

By following these steps, you should be able to start the project on your local machine. Remember to consult your project's documentation or frontend team lead for any project-specific instructions or configurations.

## Branching and Version Control Strategy

## `development`

-   **Purpose**: The primary development branch where ongoing work and features are integrated.
-   **Access**: Open to all team members for collaborative development.
-   **Merge Destination**:
    -   `master`: For stable releases.
    -   `deployment`: For testing deployments.
    -   Feature branches: For integrating new features and bug fixes.

## `master`

-   **Purpose**: The main branch for stable and production-ready code.
-   **Access**: Restricted to team lead privileges.
-   **Merge Source**: Merged from `development` after thorough testing.
-   **Deployment**: This branch is used for deploying the project to production.

## `deployment`

-   **Purpose**: A pre-production branch used for testing deployment pipelines.
-   **Access**: Restricted to team lead privileges.
-   **Merge Source**: Merged from `development` to prepare for deployment.
-   **Deployment**: This branch is used to test deployment processes and ensure smooth production deployments using pipelines.

## Feature Branches

-   **Purpose**: Created for developing specific features, bug fixes, or tasks.
-   **Access**: Open to team members for individual feature development.
-   **Merge Destination**: Typically merged into the `development` branch once work is completed and tested.

Branches play a crucial role in your project's development lifecycle, ensuring that code changes are properly managed, tested, and deployed to production.

**Note:** It is essential to follow the established branching and merging workflow to maintain code quality and stability throughout the development process.

1 / 1

In our project, we follow a version control strategy that emphasizes organization, collaboration, and traceability. Below are the key aspects of our branching and version control strategy:

### Branching Strategy

We use a branch-per-task strategy to manage our codebase efficiently. This approach allows us to isolate and work on individual tasks or features independently. Here are the key points to note:

1.  **Branch Naming**: While there are no strict rules for branch naming, we recommend following a structured approach for easier tracking and debugging. Branch names should include a task title and the associated task ID from our project management tool, such as Jira. For example: `task-title/task-id-123123`.
2.  **Branch Creation**: Whenever you start working on a new task or feature, create a new branch based on the development branch. This ensures that your branch includes the latest changes from the development branch.
3.  **Commits**: We encourage the use of atomic commits. Each commit should represent a single, logical change or improvement. This makes it easier to track changes, understand the commit history, and facilitates debugging.
4.  **Gitignore**: Make sure to include a `.gitignore` file in your project to specify files and directories that should be excluded from version control. This helps keep the repository clean and avoids unnecessary files being tracked.

### Merge Requests

After completing a task or feature, you should create a merge request. Here are the key points for merge requests:

1.  **Target Branch**: Merge requests should target the development branch. This ensures that your changes are integrated into the latest version of the application.
2.  **Branch Deletion**: Do not delete your branch after the merge request is accepted. Keeping the branch allows for future reference and potential bug fixes or updates related to that task.
3.  **Commit Squashing**: By default, we do not squash commits in the branch. Each commit represents a specific change, and this history can be valuable for understanding the development process. However, if commit squashing is necessary for specific reasons, the team lead will provide guidance.

### Collaboration and Communication

Effective communication and collaboration are essential in our version control strategy. Team members should actively communicate with the team lead and each other, especially when encountering issues or needing clarification on tasks.

By following these guidelines, we can maintain a well-organized and efficient version control system that promotes collaboration and simplifies the tracking and management of tasks and features within the project.

# Table Component Documentation

The `Table` component is a versatile and customizable table view designed to display data with various features such as filtering, pagination, and expandable rows. It can be easily integrated into your web application to present tabular data effectively.

## Props

The `Table` component accepts the following props:

-   `infoTable`: An array containing information about the table columns, including column titles, field names, and optional custom rendering functions.
-   `url`: The API endpoint URL used to fetch data for the table.
-   `noFilter`: A boolean indicating whether to display the filter controls.
-   `filterParam`: An object containing additional filter parameters to be included in API requests.
-   `collapseUrl`: The API endpoint URL used to fetch collapse content for expandable rows.
-   `getData`: A function to fetch data from the specified URL.
-   `resultData`: Data received from API requests.
-   `collapsible`: A boolean indicating whether rows can be expanded.
-   `collapseRequest`: A function to fetch collapse content for an expandable row.
-   `collapseContent`: Content to display in the expandable row.
-   `footer`: Footer content to be displayed at the bottom of the table.
-   `data`: An array of data objects to populate the table directly (useful for static data).
-   `pageSize`: The number of rows to display per page.
-   `totalPage`: The total number of pages in the data set.
-   `totalCount`: The total number of data items.
-   `currentPage`: The current page number.
-   `noPagination`: A boolean indicating whether to hide pagination controls.
-   `getDataCallbackFilter`: A function to fetch data when filters are applied.
-   `urlCallbackFilter`: The API endpoint URL used for fetching filtered data.
-   `defaultPageSize`: The default number of rows to display per page.
-   `width`: The width of the table.

## FilterTable Component

The `FilterTable` component displays filter controls for the table. It allows users to refine their data view based on various criteria.

## HeadTable Component

The `HeadTable` component renders the table's header row, including column titles.

## BodyTable Component

The `BodyTable` component generates the main body of the table, displaying data rows. It supports features like collapsible rows and custom cell rendering.

## PaginateCustom Component

The `PaginateCustom` component renders pagination controls, enabling users to navigate through multiple pages of data. It also includes options to customize the number of rows displayed per page.

## Usage

To use the `Table` component in your project, follow these steps:

1.  Import the `Table` component into your component or page where you want to display the table.

javascriptCopy code

`import Table from './Table'; // Replace with the actual path to the Table component.`

2.  Pass the necessary props to the `Table` component to configure its behavior and appearance.

javascriptCopy code

`<Table   infoTable={infoTableData}   url="/api/data"   // Other props... />`

3.  Customize the `infoTableData` array to define your table's columns and their properties.
4.  Implement API calls, data fetching, and filter functionality as needed in your application.

By integrating the `Table` component and its related components into your project, you can easily create interactive and data-rich tables with features like filtering, pagination, and expandable rows.

ChatGPT

# Breadcrumb Setter Component Documentation

The Breadcrumb Setter Component is a dynamic and versatile utility for setting breadcrumbs in your React application. It is designed to create breadcrumbs based on the user's journey through the application, utilizing the React Router DOM's navigation state logic. Breadcrumbs provide users with a clear path to navigate back to previous pages or sections of the application.

## Features

-   Dynamically set breadcrumbs based on user interactions and routes.
-   Supports both simple and complex breadcrumb structures.
-   Utilizes React Router DOM for navigation and state management.
-   Customizable breadcrumb appearance with optional icons.
-   Supports status indicators for breadcrumb items (e.g., "Pending," "Accepted," "Rejected").

## Component Overview

The Breadcrumb Setter Component consists of the following main elements:

1.  **useBreadCrumb Hook**:
    -   `setBreadCrumb`: A function to set the breadcrumb data dynamically.
    -   `BreadcrumbHead`: Component to display the breadcrumb header, including text and status indicators.
    -   `BreadcrumbContent`: Component to render the breadcrumb trail, allowing users to navigate back to previous pages.

## Usage

To use the Breadcrumb Setter Component in your application, follow these steps:

1.  Import the necessary components and icons into your component or page where you want to use breadcrumbs.

javascriptCopy code

`import { useBreadCrumb } from './BreadcrumbSetter'; // Replace with the actual path to the Breadcrumb Setter component. import { EyeIcon } from '@/assets/icon'; // Import icons if needed.`

2.  Initialize the Breadcrumb Setter Hook to access its functions and components.

javascriptCopy code

`const { setBreadCrumb, BreadcrumbHead, BreadcrumbContent } = useBreadCrumb();`

3.  Use the `setBreadCrumb` function to dynamically set breadcrumb data based on user interactions and routes. This function accepts an object with breadcrumb information, including text, status, and a back button function (if needed).

javascriptCopy code

`setBreadCrumb({   textHead: 'کالا مجوز حقوق و عوارض', // Breadcrumb header text   status: 0, // Status indicator (0: Pending, 1: Accepted, 2: Rejected)   backBtn: () => {     // Custom back button logic (if needed)   }, });`

4.  Use the `BreadcrumbHead` component to display the breadcrumb header, including the text and status indicators. You can customize the appearance of the header based on the breadcrumb data.

javascriptCopy code

`<BreadcrumbHead />`

5.  Use the `BreadcrumbContent` component to render the breadcrumb trail, allowing users to navigate back to previous pages. This component takes an optional `staticLastStepper` prop for a static breadcrumb step.

javascriptCopy code

`<BreadcrumbContent staticLastStepper="کالا مجوز حقوق و عوارض" />`

6.  To set breadcrumbs dynamically based on user interactions, use the `navigate` function from React Router DOM in your click event handler. Pass the breadcrumb information as part of the `state` object.

javascriptCopy code

`` <div   className="cursor-pointer"   onClick={() =>     navigate(`/cartable/${RouteMap.cartable.productLicenseRightsDutiesDetail}/${requestNumber}/${goodsCode}`, {       state: [         ...(location.state || []),         ['کالا مجوز حقوق و عوارض', `${location.pathname}${location.search}`],       ],     })   } >   <EyeIcon /> </div> ``

By following these steps, you can easily implement a dynamic breadcrumb navigation system in your React application, providing users with a clear and intuitive way to navigate through your application's complex routes and sections.

# Toast Notification Component Documentation

The Toast Notification Component is a utility for displaying toast notifications in your React application based on API response data. Toast notifications provide users with feedback about the success or failure of their actions within the application.

## Features

-   Automatically displays toast notifications based on API response data.
-   Customizable toast appearance with different colors and icons.
-   Supports success and error notifications.
-   Optional loading indicator during API requests.

## `HandleFetch` Component

The `HandleFetch` component is responsible for handling API response data and triggering toast notifications based on the response. It includes the following props:

-   `data`: The API response data object that contains information about the success, error, or loading status.
-   `notif`: An object that configures which types of notifications to display (`flagSuccess` and `flagError`).
-   `loadingTitle`: An optional title to display during loading, indicating that an API request is in progress.

### Usage

To use the `HandleFetch` component in your application, follow these steps:

1.  Use the `HandleFetch` component and pass the required props (`data`, `notif`, and optionally `loadingTitle`) to handle API response data and trigger toast notifications.

javascriptCopy code

`<HandleFetch   data={apiResponseData}   notif={{ flagSuccess: true, flagError: true }}   loadingTitle="Loading..." // Optional />`

2.  Customize the `notif` object to control which types of notifications should be displayed. Set `flagSuccess` and `flagError` to `true` or `false` as needed.

### Toast Notifications

The toast notifications triggered by the `HandleFetch` component are configured using Redux and the `toastSlice` reducer. The reducer stores the toast state, including the list of toast notifications and their appearance settings.

## `showToast` Action

The `showToast` action is used to update the toast state with new toast notifications. It accepts an object with the following properties:

-   `toastList`: An array of toast notification objects. Each object contains the following properties:

    -   `borderColor`: The border color of the toast notification.
    -   `backgroundColor`: The background color of the toast notification.
    -   `description`: The text description of the notification.
    -   `icon`: The icon to display (e.g., 'success' or 'error').
    -   `title`: The title of the notification.

-   `position`: The position of the toast notifications (default is 'top-right').
-   `autoDelete`: A boolean indicating whether to automatically delete notifications after a set time (default is `true`).
-   `autoDeleteTime`: The time (in milliseconds) after which notifications should be automatically deleted (default is 3000ms).

## Usage

To use the toast notifications in your application, follow these steps:

1.  Import the Redux `showToast` action into your component or page.

javascriptCopy code

`import { showToast } from '@/redux/slice/toastSlice'; // Import the showToast action.`

2.  Dispatch the `showToast` action with the desired toast notification configuration.

javascriptCopy code

`dispatch(   showToast({     toastList: [       {         borderColor: 'green-150',         backgroundColor: 'bg-green-350',         description: 'Operation completed successfully',         icon: 'success',         title: 'Success',       },     ],   }) );`

By following these steps, you can easily integrate toast notifications into your React application to provide users with feedback on their actions and interactions with the application's API.

# ViewFile Component Documentation

The `ViewFile` component is a React component used to display import, export, or transit cartable views in your application. It dynamically generates tabs based on the type of cartable (import, export, transit) and displays content for each tab. The component also sets breadcrumbs and handles indicator badges for each tab.

## Features

-   Dynamic generation of tabs based on the type of cartable.
-   Display of specific content for each tab.
-   Breadcrumb setting based on the cartable type.
-   Indicator badges to show items that are not accepted or rejected in the "final accept or final reject" step.

# Project Folder Structure Documentation

Your project follows a well-organized folder structure that separates various sections of your application, including `export`, `import`, and `transit`. Within each of these sections, there are `cartable` folders and `viewFile` folders. This documentation will provide an overview of your project's folder structure.

## Folder Structure Overview

### Export Section

-   **`export`**: The root folder for the export section.
    -   **`cartable 1`**: A folder containing files and components related to the first export cartable.
    -   **`cartable 2`**: A folder containing files and components related to the second export cartable.
    -   **`viewFile`**: A folder containing components specific to the export view file functionality.
        -   **`viewfile tab component`**: Components representing individual tabs within the export view file.

### Import Section

-   **`import`**: The root folder for the import section.
    -   **`cartable 1`**: A folder containing files and components related to the first import cartable.
    -   **`cartable 2`**: A folder containing files and components related to the second import cartable.
    -   **`viewFile`**: A folder containing components specific to the import view file functionality.
        -   **`viewfile tab component`**: Components representing individual tabs within the import view file.

### Transit Section

-   **`transit`**: The root folder for the transit section.
    -   **`cartable 1`**: A folder containing files and components related to the first transit cartable.
    -   **`cartable 2`**: A folder containing files and components related to the second transit cartable.
    -   **`viewFile`**: A folder containing components specific to the transit view file functionality.
        -   **`viewfile tab component`**: Components representing individual tabs within the transit view file.

## Usage

This folder structure promotes a modular and organized approach to managing different sections of your application. It allows for easy navigation and maintenance of code related to each cartable and view file component.

ChatGPT

# RTK Query Services Structure

In your project, you have a structured RTK Query service setup that manages various API services based on different base URLs. Each service is categorized under different folders, such as `exc`, `exq`, `transit`, etc. Below, we'll describe the structure and functionality of these services.

## Folder Structure

Your folder structure is organized as follows:

-   **Service Folder (e.g., `exc`, `exq`, `transit`, etc.)**
    -   Each service folder represents a specific area of your application, and it contains API services related to that area.

### Components of a Service

-   **`crudDataApi`**: This is the API service instance created using `createApi`. It contains the following properties:

    -   `reducerPath`: Specifies the name of the slice in your Redux store where the service data will be stored.
    -   `baseQuery`: Defines the base query function that fetches data from the API. It includes the base URL and headers configuration.
    -   `endpoints`: Specifies the API endpoints available in this service.

-   **`getData`**: This is a query endpoint for fetching data. It defines how to construct the query URL and parameters.
-   **`postData`**: This is a mutation endpoint for sending POST requests. It defines the URL, HTTP method, query parameters, and request body.
-   **Hooks (e.g., `useLazyGetDataQuery`, `useGetDataQuery`, `usePostDataMutation`)**: These hooks are generated automatically by RTK Query based on your service endpoints. They can be used in your components to fetch data and make mutations.

This structured RTK Query service setup allows you to:

-   Organize your API services based on different base URLs or application areas.
-   Define API endpoints for various CRUD operations (e.g., `getData`, `postData`) within each service.
-   Use generated hooks to easily interact with these services in your React components.
-   Maintain a clean and modular project structure, making it easier to manage and extend your API services as your project grows.

Overall, this approach simplifies API integration, enhances code maintainability, and improves the separation of concerns in your project.

# Utility Functions Documentation

Below are descriptions of the utility functions in your project's utility functions folder. These functions are designed to handle various tasks and conversions. This documentation provides an overview of each function's purpose and usage.

## `uniqueID`

-   **Description**: Generates a unique ID composed of a timestamp and a random string.
-   **Usage**: Used to create unique identifiers, such as for keys in lists or unique references.

## `convertPersianDigitInEnglish`

-   **Description**: Converts Persian and Arabic digits in a string to English digits.
-   **Usage**: Useful for standardizing digit representation for processing or display.

## `convertDateShamsiToMiladi`

-   **Description**: Converts a Shamsi (Jalaali) date to a Gregorian (Miladi) date.
-   **Usage**: Useful for converting dates between different calendar systems.

## `convertDateMiladiToShamsi`

-   **Description**: Converts a Gregorian (Miladi) date to a Shamsi (Jalaali) date.
-   **Usage**: Complementary to `convertDateShamsiToMiladi`, allowing bidirectional date conversion.

## `formatNumber`

-   **Description**: Formats a number with thousands separators.
-   **Usage**: Useful for displaying numbers in a more readable format, e.g., 1,000,000.

## `convertEnglishNumberToPersian`

-   **Description**: Converts English digits in a string to Persian digits.
-   **Usage**: Useful for displaying numbers using Persian numerals for localization.

## `parseDate`

A collection of date parsing functions:

-   `getDate(date)`: Returns the formatted date portion (e.g., "1402/06/15").
-   `getTime(date)`: Returns the formatted time portion (e.g., "14:30:00").
-   `getFullDate(date)`: Returns both date and time portions (e.g., "1402/06/15 - 14:30:00").
-   `getTimeLeft(from, to)`: Calculates the time difference in days between two dates.
-   `secondsToHms(d)`: Converts seconds to HH:MM:SS format.

These functions are helpful for parsing and formatting date and time values for display or calculations.

---
#   m j - p r o j  
 #   m j - p r o j  
 #   m j - p r o j - 2  
 #   m j - p r o j - 2  
 
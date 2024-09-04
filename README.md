# FetchHiring
This Android application fetches data from an external API and displays it in a user-friendly list format using Jetpack Compose. The app is designed with modern Android development best practices, including clean architecture, dependency injection with Hilt, caching with Room database, and efficient data loading with the Paging 3 library.

**Features**

1. Fetch and Display Data: Fetches items from a remote API and displays them grouped by listId, sorted by listId and name.
2. Paging with Jetpack Compose: Uses Paging 3 library to display data efficiently and handle large datasets.
3. Local Caching: Caches fetched data in a local Room database, ensuring smooth performance and offline capabilities.
4. Filtering: Filters out items where name is blank or null.
5. List Animations: Adds animations for list items, enhancing the user experience.
6. Dependency Injection with Hilt: Manages dependencies using Hilt, simplifying code and improving testability.
7. Modern UI with Jetpack Compose: Uses Jetpack Compose for building declarative, responsive, and interactive UI components.

Libraries Used

1. Jetpack Compose
Version: 1.6.0
Description: Modern toolkit for building native Android UIs with declarative components, enabling a more intuitive and efficient development process.
2. Room
Version: 2.6.0
Description: A robust SQLite object-mapping library that provides an abstraction layer for local database access, ensuring seamless integration with Kotlin Coroutines and Flow for reactive programming.
3. Paging 3
Version: 3.2.0
Description: Helps load and display data in small chunks, making it easier to handle large data sets and display data efficiently in lists.
4. Dagger Hilt
Version: 2.48
Description: A dependency injection library that simplifies DI setup in Android apps, improving code readability, modularity, and testability.
5. Retrofit 2
Version: 2.9.0
Description: A type-safe HTTP client for Android that makes it easy to consume RESTful APIs, integrated with Gson for parsing JSON responses.
6. OkHttp Logging Interceptor
Version: 4.11.0
Description: Provides a logging mechanism for OkHttp requests and responses, which is useful for debugging network interactions.
7. Kotlin Coroutines
Version: 1.7.3
Description: Supports asynchronous programming, enabling easy management of background tasks, such as fetching data from the network.

**Getting Started**

Prerequisites
1. Android Studio: Make sure you have the latest stable version of Android Studio installed.
2. Gradle: The project is configured to use Gradle Version Catalogs with a libs.versions.toml file for dependencies management.
Installation

**Download the code from Repository**

git clone https://github.com/yourusername/fetch-items-app.git
cd fetch-items-app
Open the Project in Android Studio

Open Android Studio, click on Open, and select the project directory you just cloned.

Sync the Project

Android Studio will automatically prompt you to sync the project. If not, click on Sync Project with Gradle Files in the toolbar.
Run the App

Select a device or emulator and click the Run button in Android Studio.
Configuration
API Endpoint: The app fetches data from the URL https://fetch-hiring.s3.amazonaws.com/hiring.json. You can modify this endpoint in the ApiService.kt file if needed.
Troubleshooting
Build Errors: Ensure all dependencies are properly synced. If you encounter any build issues, try cleaning and rebuilding the project by selecting Build > Clean Project and then Build > Rebuild Project.

Internet Permission: Make sure that your AndroidManifest.xml includes the required permissions:

xml
Copy code
<uses-permission android:name="android.permission.INTERNET"/>
Project Structure
model/: Contains the data model class (Item.kt).
data/: Contains Room database setup (ItemDao.kt, ItemDatabase.kt).
network/: Contains API service definitions and Retrofit setup (ApiService.kt, RetrofitInstance.kt).
repository/: Contains the repository class (ItemRepository.kt) that handles data operations.
viewmodel/: Contains the ViewModel (ItemViewModel.kt) that manages UI-related data in a lifecycle-conscious way.
ui/: Contains the Compose UI components (ItemScreen.kt) that render the data to the user.
Contribution
Feel free to contribute to this project by submitting issues or pull requests. Any improvements, bug fixes, or new features are welcome.

License
This project is licensed under the MIT License - see the LICENSE file for details.

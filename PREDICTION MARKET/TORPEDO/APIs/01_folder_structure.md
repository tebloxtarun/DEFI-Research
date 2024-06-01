1. **app**
   - **assets**: Contains assets like JavaScript, CSS, and images.
     - **config**: Configuration for asset pipeline.
     - **images**: Images used in the application.
     - **stylesheets**: CSS stylesheets used in the application.
   - **channels**: Action Cable channels for handling WebSocket connections.
   - **controllers**: Contains controllers that handle requests and orchestrate the application's flow.
     - **admin**: Controllers for administrative tasks.
     - **api**: Controllers for handling API requests.
     - **concerns**: Shared controller concerns.
   - **helpers**: Helper modules containing utility methods for views and controllers.
   - **javascript**: JavaScript files and packs for front-end functionality.
     - **channels**: Action Cable JavaScript channels.
     - **packs**: JavaScript entry points managed by Webpacker or Sprockets.
   - **jobs**: Active Job classes for handling asynchronous tasks.
   - **mailers**: Contains mailer classes for sending emails.
   - **models**: Object-relational mapping (ORM) classes representing data entities.
     - **concerns**: Shared model concerns.
   - **serializers**: Classes or modules for serializing model data into JSON or other formats.
   - **services**: Contains service classes or modules for handling business logic.
     - **bepro**: Service related to BEPRO network integration.
     - **discord**: Service related to Discord integration.
     - **subgraph**: Service related to interacting with subgraphs.
   - **views**: HTML templates or views rendered by controllers (typically used in server-rendered applications).
   - **workers**: Background workers or job processors.

2. **bin**: Executable scripts and binaries.

3. **config**: Configuration files for Rails and other libraries.
   
4. **db**: Database schema and migrations.

5. **lib**: Libraries and extensions not necessarily part of Rails convention.

6. **log**: Application log files.

7. **public**: Static files served directly by the web server.

8. **storage**: Active Storage files (if used).

9. **tmp**: Temporary files.

10. **vendor**: Third-party libraries and dependencies.

| Directory     | Purpose                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Controllers** | Handle incoming requests, process data, and render views or JSON responses.                                                                               |
| **Models**      | Represent data structures and manage interactions with the database.                                                                                      |
| **Views**       | HTML templates rendered by controllers to generate the final output sent to clients.                                                                      |
| **Helpers**     | Provide utility functions used across views and controllers.                                                                                              |
| **Assets**      | Manage JavaScript, CSS, and image assets for the application.                                                                                              |
| **Jobs**        | Perform background tasks or jobs asynchronously.                                                                                                           |
| **Mailers**     | Construct and send emails from the application.                                                                                                            |
| **Services**    | Encapsulate business logic or external integrations to keep controllers thin.                                                                              |
| **Config**      | Configuration files for Rails, databases, and other settings.                                                                                              |
| **DB**          | Store database schema, migrations, and seed data.                                                                                                           |
| **Lib**         | Extend Rails with additional libraries or custom code.                                                                                                      |
| **Log**         | Record application logs.                                                                                                                                  |
| **Public**      | Serve static files like error pages, images, and other non-Rails assets.                                                                                   |
| **Storage**     | Store files managed by Active Storage.                                                                                                                     |
| **Tmp**         | Temporary files used by the application.                                                                                                                   |
| **Vendor**      | Store third-party libraries and dependencies managed outside of Bundler.                                                                                   |

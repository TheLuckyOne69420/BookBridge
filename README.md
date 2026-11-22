# BookBridge Final Integration

This version integrates the TSA2 domain model with JDBC persistence and a Swing interface.

## Run requirements

Java 8 or newer and the SQLite JDBC driver (`org.xerial:sqlite-jdbc`) are required. Add the driver JAR to the project libraries. The application creates `bookbridge.db` automatically.

## Run

Compile all `.java` files with the SQLite driver on the classpath, then run `Main`. The UI supports catalog management, member management, issuing, returning, reservations, cancellation, search, refresh, and circulation reports.

## Architecture

`BookBridgeFrame` is the presentation layer. `LibraryService` contains business rules and JDBC transactions. `Database` owns connections and schema initialization. The model classes enforce basic invariants.

# Crystal Oasis Hotel Management System

## Database Setup

This project requires the database file:

```txt
Hotel_Management_System.bacpac
```

### Import Database into SQL Server Management Studio (SSMS)

1. Open SQL Server Management Studio (SSMS).
2. Connect to:
```txt
Your Server name\SQLEXPRESS
```

3. In Object Explorer, right-click:

```txt
Databases
```

4. Select:

```txt
Import Data-tier Application
```

5. Click **Next**.
6. Choose:

```txt
Import from local disk
```

7. Browse and select:

```txt
Hotel_Management_System.bacpac
```

8. Click **Next** until the import process finishes.
9. Verify that the database appears under:

```txt
Databases
 └── Hotel_Management_System
```

---

## Database Connection Configuration

Open the file containing the database configuration:

```txt
DatabaseConfig.cs
```

Locate the following line:

```csharp
public static string connectionString = "...";
```

Replace it with:

```csharp
public static string connectionString =
@"Data Source=Your Server name\SQLEXPRESS;
Initial Catalog=Hotel_Management_System;
Integrated Security=True;";
```

---

## Build and Run

1. Save all files.
2. Build the solution:

```txt
Ctrl + Shift + B
```

3. Run the application:

```txt
F5
```

---

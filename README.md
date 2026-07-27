# User Configuration Manager

A simple Python application that allows users to manage their configuration settings such as theme, language, notifications, and other preferences.

## Features

- Add a new setting
- Update an existing setting
- Delete a setting
- View all current settings
- Automatic conversion of keys and values to lowercase
- Prevents duplicate settings
- User-friendly success and error messages

## Project Structure

```
UserConfigurationManager/
│
├── user_configuration_manager.py
└── README.md
```

## Functions

### add_setting(settings, setting)

Adds a new key-value pair to the settings dictionary.

**Parameters**
- `settings` : Dictionary containing user settings
- `setting` : Tuple containing `(key, value)`

**Returns**
- Success message if the setting is added.
- Error message if the key already exists.

Example:

```python
settings = {}
print(add_setting(settings, ("Theme", "Dark")))
```

Output:

```
Setting 'theme' added with value 'dark' successfully!
```

---

### update_setting(settings, setting)

Updates an existing setting.

**Parameters**
- `settings` : Dictionary containing user settings
- `setting` : Tuple containing `(key, value)`

**Returns**
- Success message if updated.
- Error message if the setting does not exist.

Example:

```python
print(update_setting(settings, ("Theme", "Light")))
```

---

### delete_setting(settings, key)

Deletes a setting from the dictionary.

**Parameters**
- `settings`
- `key`

**Returns**
- Success message if deleted.
- "Setting not found!" if the key does not exist.

Example:

```python
print(delete_setting(settings, "Theme"))
```

---

### view_settings(settings)

Displays all user settings.

**Parameters**
- `settings`

**Returns**
- "No settings available." if empty.
- Formatted list of settings otherwise.

Example:

```python
print(view_settings(settings))
```

Output:

```
Current User Settings:
Theme: dark
Language: english
Notifications: enabled
```

---

## Requirements

- Python 3.x

No external libraries are required.

## How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/user-configuration-manager.git
```

2. Navigate to the project folder

```bash
cd user-configuration-manager
```

3. Run the program

```bash
python user_configuration_manager.py
```

---

## Sample Test Data

```python
test_settings = {
    "theme": "dark",
    "language": "english",
    "notifications": "enabled"
}
```

---

## Sample Output

```
Setting 'volume' added with value 'high' successfully!
Setting 'theme' updated to 'light' successfully!
Setting 'language' deleted successfully!

Current User Settings:
Theme: light
Notifications: enabled
Volume: high
```

---

## Learning Objectives

This project demonstrates:

- Python Functions
- Dictionaries
- Tuples
- String Manipulation
- Conditional Statements
- Dictionary Operations
- Code Organization
- Basic CRUD (Create, Read, Update, Delete) Operations

---

## License

This project is created for educational purposes as part of the freeCodeCamp Python Certification.

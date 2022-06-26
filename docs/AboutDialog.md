# AboutDialog

The `AboutDialog` offers a simple way to display information about a program like its logo, name, copyright, website and license. It is also possible to give credits to the authors, documenters, translators and artists who have worked on the program. An about dialog is typically opened when the user selects the `About` option from the `Help` menu(`Help` -> `About`). All parts of the dialog are optional.

![About Dialog](/img/aboutdialog.png)

### Creation

The creation method is used to create an instance of the class or widget.

```vala
var dialog = new Gtk.AboutDialog();
```

### Properties

An instance of `AboutDialog` supports following properties.

#### artists

```
string[] artists { get; set; }

// Example
dialog.artists = {"Darkwing Duck", "Launchpad McQuack"};
```

The people who contributed artwork to the program, as a null-terminated array of strings.

#### authors

```
string[] authors { get; set; }

// Example
dialog.authors = {"Scrooge McDuck", "Gyro Gearloose"};
```

The authors of the program, as a null-terminated array of strings.

#### comments

```
string comments { get; set; }

// Example
dialog.comments = "Scrooges wealth management system";
```

Comments about the program.

#### copyright

```
string copyright { get; set; }

// Example
dialog.copyright = "Copyright © 1998-2000 Gyro Gearloose";
```

Copyright information for the program.

#### documenters

```
string[] documenters { get; set; }

// Example
dialog.documenters = null; // Real inventors don't document.
```

The people documenting the program, as a null-terminated array of strings.

#### license

```
string license { get; set; }


// Example
dialog.license = "Permission is hereby granted, NOT free of charge, ..., very long text";
```

The license of the program.

#### license_type

```
License license_type { get; set; }
```

The license of the program, as a value of the gtklicense enumeration.

#### logo

```
Pixbuf logo { get; set; }
```

A logo for the about box.

#### logo_icon_name

```
string logo_icon_name { get; set; }
```

A named icon to use as the logo for the about box.

#### program_name

```
string program_name { get; set; }

// Example
dialog.program_name = "SWMS";
```

The name of the program.

#### translator_credits

```
string translator_credits { get; set; }

// Example
dialog.translator_credits = null; // We only need a scottish version.
```

Credits to the translators.

#### version

```
string version { get; set; }

// Example
dialog.version = "3.0";
```

The version of the program.

#### website

```
string website { get; set; }

// Example
dialog.website = "http://en.wikipedia.org/wiki/Scrooge_McDuck";
```

The URL for the link to the website of the program.

#### website_label

```
string website_label { get; set; }

// Example
dialog.website_label = "Scrooge McDuck and Co.";
```

The label for the link to the website of the program.

#### wrap_license

```
bool wrap_license { get; set; }

// Example
dialog.wrap_license = true;
```

Whether to wrap the text in the license dialog.

### Methods

An instance of `AboutDialog` supports following methods.

#### add_credit_section

```
public void add_credit_section(string section_name, string[] people)
```

Creates a new section in the Credits page.

#### get_artists

```
public string[] get_artists()
```

Returns the string which are displayed in the artists tab of the secondary credits dialog.

#### set_artists

```
public void set_artists(string[] artists)
```

Sets the strings which are displayed in the artists tab of the secondary credits dialog.

#### get_authors

```
public string[] get_authors()
```

Returns the string which are displayed in the authors tab of the secondary credits dialog.

#### set_authors

```
public void set_authors(string[] authors)
```

Sets the strings which are displayed in the authors tab of the secondary credits dialog.

#### get_comments

```
public string get_comments()
```

Returns the comments string.

#### set_comments

```
public void set_comments(string? comments)
```

Sets the comments string to display in the about dialog.

#### `get_copyright`

```
public string get_copyright()
```

Returns the copyright string.

#### set_copyright

```
public void set_copyright(string? copyright)
```

Sets the copyright string to display in the about dialog.

#### get_documenters

```
public string[] get_documenters()
```

Returns the string which are displayed in the documenters tab of the secondary credits dialog.

#### set_documenters

```
public void set_documenters(string[] documenters)
```

Sets the strings which are displayed in the documenters tab of the secondary credits dialog.

#### get_license

```
public string get_license()
```

Returns the license information.

#### set_license

```
public void set_license(string? license)
```

Sets the license information to be displayed in the secondary license dialog.

#### get_license_type

```
public License get_license_type()
```

Retrieves the license set using set_license_type

#### set_license_type

```
public void set_license_type(License license_type)
```

Sets the license of the application showing the this dialog from a list of known licenses.

#### get_logo

```
public Pixbuf get_logo()
```

Returns the pixbuf displayed as logo in the about dialog.

#### set_logo

```
public void set_logo(Pixbuf? logo)
```

Sets the pixbuf to be displayed as logo in the about dialog.

#### get_logo_icon_name

```
public string get_logo_icon_name()
```

Returns the icon name displayed as logo in the about dialog.

#### set_logo_icon_name

```
public void set_logo_icon_name(string? icon_name)
```

Sets the pixbuf to be displayed as logo in the about dialog.

#### get_program_name

```
public string get_program_name()
```

Returns the program name displayed in the about dialog.

#### set_program_name

```
public void set_program_name(string name)
```

Sets the name to display in the about dialog.

#### get_translator_credits

```
public string get_translator_credits()
```

Returns the translator credits string which is displayed in the translators tab of the secondary credits dialog.

#### set_translator_credits

```
public void set_translator_credits(string? translator_credits)
```

Sets the translator credits string which is displayed in the translators tab of the secondary credits dialog.

#### get_version

```
public string get_version()
```

Returns the version string.

#### set_version

```
public void set_version(string? version)
```

Sets the version string to display in the about dialog.

#### get_website

```
public string get_website()
```

Returns the website URL.

#### set_website

```
public void set_website(string? website)
```

Sets the URL to use for the website link.

#### get_website_label

```
public string get_website_label()
```

Returns the label used for the website link.

#### set_website_label

```
public void set_website_label(string website_label)
```

Sets the label to be used for the website link.

#### get_wrap_license

```
public bool get_wrap_license()
```

Returns whether the license text in this is automatically wrapped.

#### set_wrap_license

```
public void set_wrap_license(bool wrap_license)
```

Sets whether the license text in this is automatically wrapped.

### Signals

An instance of `AboutDialog` supports following signals.

#### activate_link

```
public virtual signal bool activate_link(string uri)
```

The signal which gets emitted to activate a URI. Applications may connect to it to override the default behaviour, which is to call `show_uri_on_window`.

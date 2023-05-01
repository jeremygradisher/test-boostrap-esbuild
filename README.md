# Bootstrap test

Testing adding Bootstrap from the start with Rails 7 and esbuild:

1. Create application w bootstrap, esbuild and postgresql
```
rails new bootstrap-test --css=bootstrap --javascript=esbuild --database=postgresql
```

2. We can now run bundle install to install the correct version of the gem.
```
bundle install
```

3. Now that our application is ready, let's type the bin/setup command to install the dependencies and create the database:
```
bin/setup
```

4. We can now run the rails server, and the scripts that precompile the CSS and the JavaScript code with the bin/dev command:
```
bin/dev
```

5. We can now go to http://localhost:3000, and we should see the Rails boot screen.

6. Create a Welcome page:
```
rails generate controller Welcome index

```

7.  Adjust the route
```
root 'welcome#index'
```

8. Add some bootstrap to see if it works:
```
<div class="dropdown">
  <button class="btn btn-primary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
    Dropdown
  </button>
  <ul class="dropdown-menu">
    <li><button class="dropdown-item" type="button">Dropdown item</button></li>
    <li><button class="dropdown-item" type="button">Dropdown item</button></li>
    <li><button class="dropdown-item" type="button">Dropdown item</button></li>
  </ul>
</div>
```



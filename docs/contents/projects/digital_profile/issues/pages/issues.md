#Issues

## General overview
These are the issues occurred so far.

###Github Link
[See issues on github](https://github.com/dolpotech/digitalprofile/issues)

##Issues

1. ### requirements uninstalled (crum not found)
   
    #### `Reproduce Method` 
        once we restart project `make start_project`
    #### `Problem 1`
        old requirements were installed during image building so, few requirements like `(django-crum,altair,django-restframework)` will not be present once we run `make start_project`
    #### `Problem 2`
        Once you install missing requirements the error may persist because `kobofe_digital_beat_1` and `kobofe_digital_worker_1` containers have exited
    #### `Solution` 
        restart containers `kobofe_digital_beat_1` and `kobofe_digital_beat_1`

2. ### Docker package authentication login from terminal:
   #### `Solution` 
	docker login docker.pkg.github.com

3. ###Django project doesnot autoreload
    ### `Solution`
    `Add: py-autoreload=3 in uwsgi.ni file of dp project`
    

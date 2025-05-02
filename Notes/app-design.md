# Defintions

Django project - web applciation powered by the Django wed framework

Djagon apps - smaller libraries designed to respresetn as ingle aspect of a porject. A django project is made up of apps. Some of those apps 

Installed APPS - list of django apps used by a given project

third party django packaes - simply pluggable, reusable django apps that been packaged with Python packaging tools


# 4.1 Golden Rule of Django App Design

“The art of creating and maintaining a good Django app is that it should
follow the truncated Unix philosophy according to Douglas McIlroy: ‘Write
programs that do one thing and do it well.”’ - James Bennett

each app should be tighlty focused on its task.

If an app an't be explained in a signle sentence of moderat elength, or you need to say "and" more than once, it means the app is too big.

### 4.1.1 a practical example

twoscoops_project - name of reposiroy

flavors_app - to track all of the ice cream flavors and list them

blog app - for the official app and posts

events app - to display listings of our shops; events on our website.

Another example

shop app - allow us to sell orders by mail
tickets app - handle ticket sales for festivals

rather then expanding the shop app to include tickets, tickets gets its own app because most devents don't require tickets. 
These tickets may also contain more complex logic as the site grows.

## 4.2 Naming apps

when possible, apps should be single words

as a rule, the app's name should be a plural name of the app's amin model, but there are good excpetions. Blog being the most common one.

## 4.3 keep apps small

in parallel with micro services architecture, we want to keep our apps small

## 4.4 what modules belong in an app?

### 4.4.1 Common App Modules

```
app_name/
|-- __init.py__
|-- admin.py
|-- apps.py
|-- forms.py
|-- management/
|-- migrations/
|-- models.py
|-- templatetags/
|-- tests/
|-- urls.py
|-- views.pys
```

This is by no means mandated, but something that has arrisen over time due to conversations with django and python developers

### 4.4.2 uncommon app moduels

```
app-name/
├── api/
├── behaviors.py
├── constants.py
├── context_processors.py
├── decorators.py
├── db/
├── exceptions.py
├── fields.py
├── factories.py
├── helpers.py
├── managers.py
├── middleware.py
├── schema.py
├── signals.py
├── utils.py
├── viewmixins.py
```

## 4.5 Alternative: Ruby on Rails-Style Approaches

Ruby is roughly the same age as Django.
Powered by Ruby
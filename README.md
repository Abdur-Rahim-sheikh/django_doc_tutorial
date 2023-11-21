# Mysite desing using core django documentation tutorial

Did not add any gitignore to practice same thing on both my environment.
* admin site control for django models
* Coverage package
* Unit testing 
* Philosophy behind django models and others
    * A <strong><u> model </u></strong> is the single definitive source of information about my data. It follows DRY principle. Define & derieve things from it from anywhere.
    * Django <strong> APPS </strong> are <strong> "pluggable" </strong> we can sue an app in multiple proejects and we can distribute apps, because they don't have to be tied to a given Django installations.
    * Generative <strong> admin </strong> sites, gives interface for all models to help admin work manually.
    * We use `get_object_or_404()` instead of automatically catching the ojbectDoesNotExist or Http404. Because that will increase the "coupling" model layer to view layer. So to help loose coupling we use get_object_or_404 as well as get_list_or_404
* Alyaws return a `HttpResponseRedirect` after successfully dealing with POST data. This prevents data from being posted twice if a user hits the back button. 
    * return HttpResponseRedirect (reverse("some-view-name"),args=(arg1,arg2,....)) // reverse is used to build url using name. So it's called when we call another view from this view


## Testing philosophy
There might be more test code than application.
1) It doesn't matter, let them grow.
2) In tests redundancy is good thing.

Rules-of-thumb in testing,
1) A seperate `TestClass` for each model or view
2) A seperate `TestMethod` for each set of conditions you want to test.
3) Method name should describe their function.

##android studio tricks[Still update..]
This article is not about to tell you the familiar shortcuts you should know for daily use of android studio.It is about some meaningful methods you would wish you know under particular situations

*1* When your app crashed(unfortunately) at some users' phone ,assumed you have already do crash log handled,then from your server you may get some message like:

     java.lang.NullPointerException
    at android.databinding.PropertyChangeRegistry$1.onNotifyCallback(PropertyChangeRegistry.java:28)
    at android.databinding.PropertyChangeRegistry$1.onNotifyCallback(PropertyChangeRegistry.java:24)
    at android.databinding.CallbackRegistry.notifyCallbacks(CallbackRegistry.java:201)
     at android.databinding.CallbackRegistry.notifyFirst64(CallbackRegistry.java:122)
    at android.databinding.CallbackRegistry.notifyRemainder(CallbackRegistry.java:169)
    at android.databinding.CallbackRegistry.notifyRecurse(CallbackRegistry.java:145)
    at android.databinding.CallbackRegistry.notifyCallbacks(CallbackRegistry.java:91)
    at android.databinding.BaseObservable.notifyPropertyChanged(BaseObservable.java:62)
    ...

What a mess!

Generally,many people will check the log above and search from this cluster. Then find the class and go to the line where the crash happened.Well,here is a time-saving method:copy the whole log, and in android studio click Ctrl + shift +A [in mac,it's Command + shift +A],input sync,chooses "Analyze Stacktrace..." here you go~ 
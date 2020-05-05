# ConnectivityLiveData
Android LiveData that wraps a connection listener

Usage in a `Fragment`:

    ConnectivityLiveData(context).observe(viewLifecycleOwner, Observer { connectionState ->
        when (connectionState) {
            CONNECTED -> {
                // Connected to the Internet
            }
            DISCONNECTED -> {
                // Disconnected from the Internet. This is anything, but flight mode.
            }
            FLIGHT_MODE -> {
                // Device is in flight mode, but also disconnected of course.
            }
        }
    })

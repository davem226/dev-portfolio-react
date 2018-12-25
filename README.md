# dev-portfolio-react

# 1. App Skeleton
# Components
    App
        Desktop
            onclick
            File
                icon
                name
                onclick
            File

            Window
                NameBar
                    icon
                    name

                    WindowButtons
                        MinButton
                            WindowButtonContent
                            WindowButtonContent
                            onclick
                        MinButton
                        MaxButton
                            WindowButtonContent
                            WindowButtonContent
                            onclick
                        MaxButton
                        CloseButton
                            WindowButtonContent
                                exit-icon
                            WindowButtonContent
                            onclick
                        CloseButton
                    WindowButtons
                NameBar

                OptionsBar
                    options-array
                OptionsBar

                DisplayArea
                    files
                DisplayArea

                FooterBar
                    text
                FooterBar
            Window
        Desktop

        Taskbar
            StartButton
                icon
                "Start"
                onclick
            StartButton

            OpenWindowsArea
                WindowBar
                    icon
                    name
                    onclick
                WindowBar
            OpenWindowsArea

            TimeArea
                time
                icon
            TimeArea
        Taskbar
    App

# 2. API design
# On Load
    Call and await API.getFiles("Desktop")
        => Makes GET request to "/Desktop"
            => Finds all in database where Path === "/Desktop"
    Set all info on Desktop files to state
        => State passed to File Components as props
    Set "focus" to Desktop

# On Directory double-click
    Get files from Path/To/

# 3. Structure of state
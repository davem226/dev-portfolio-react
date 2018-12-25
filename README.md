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
                name
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
        Makes GET request to "/Desktop"
            Finds all in database where Path === "/Desktop"
    setState
        Add all file info
        Set "focus" to "Desktop"

# On Directory double-click
    Call openWindow("Desktop/Path/To/Directory")
        Call and await API.getFiles("Desktop/Path/To/Directory")
        setState
            Add all file info
            Push "Desktop/Path/To/Directory" to "openWindows."
            Set "focus" to "Desktop/Path/To/Directory"

# On File double-click
    Call openFile("Desktop/Path/To/File")
        switch(file.ext)
            case txt, openTextEdit(file.text)
            case ie, openPageInNewTab(file.link)
            default, cannotOpenFile(file.ext)



# 3. Achieving double-click functionality
    
# 4. Structure of state
# johnnychanjx
###### \java\seedu\address\storage\AddressBookStorage.java
``` java
    void backupAddressBook(ReadOnlyAddressBook addressBook) throws IOException;
```
###### \java\seedu\address\storage\StorageManager.java
``` java
    public void backupAddressBook(ReadOnlyAddressBook addressBook) throws IOException {
        addressBookStorage.backupAddressBook(addressBook);
    }

    //@author
    @Override
    @Subscribe
    public void handleAddressBookChangedEvent(AddressBookChangedEvent event) {
        logger.info(LogsCenter.getEventHandlingLogMessage(event, "Local data changed, saving to file"));
        try {
            saveAddressBook(event.data);
        } catch (IOException e) {
            raise(new DataSavingExceptionEvent(e));
        }
    }

}
```
###### \java\seedu\address\storage\XmlAddressBookStorage.java
``` java
    @Override
    public void backupAddressBook(ReadOnlyAddressBook addressBook) throws IOException {
        saveAddressBook(addressBook, filePath + ".backup");

    }
```
###### \resources\StudentPage\Johnny Chan.html
``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Helvetica'>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">


<style>
html,body,h1,h2,h3,h4,h5,h6 {font-family: "Helvetica", sans-serif}
</style>
<body class="w3-light-grey">

<!-- Page Container -->
<div class="w3-content w3-margin-top" style="max-width:1400px;">

    <!-- The Grid -->
    <div class="w3-row-padding">

        <!-- Left Column -->
        <div class="w3-third">

            <div class="w3-white w3-text-grey w3-card-4">
                <div class="w3-display-container">
                    <img src="../docs/images/johnnychanjx.png" style="width:100%" alt="Avatar">

                </div>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>Johnny Chan</p>
                    <p><i class="fa fa-folder-o fa-fw w3-margin-right w3-large w3-text-teal"></i>S9191911F</p>
                    <p><i class="fa fa-home fa-fw w3-margin-right w3-large w3-text-teal"></i>10 Tampines North Street 3 Singapore 461110 </p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96992220</p>
                    <hr>



                    <p class="w3-large"><b><i class="fa fa-asterisk fa-fw w3-margin-right w3-text-teal"></i>Current Subjects</b></p>
                    <p>$subject1</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent1%">$grade1</div>
                    </div>
                    <p>$subject2</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent2%">
                            <div class="w3-center w3-text-white">$grade2</div>
                        </div>
                    </div>
                    <p>$subject3</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent3%">$grade3</div>
                    </div>
                    <p>$subject4</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent4%">$grade4</div>
                    </div>
                    <p>$subject5</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent5%">$grade5</div>
                    </div>
                    <p>$subject6</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent6%">$grade6</div>
                    </div>

                    <hr>
                </div>
            </div><br>

            <!-- End Left Column -->
        </div>

        <!-- Right Column -->
        <div class="w3-twothird">

            <div class="w3-container w3-card w3-white w3-margin-bottom">



                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-address-card-o fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Next of Kin Details</h2>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>Jonathan Doe</p>
                    <p><i class="fa fa-genderless fa-fw w3-margin-right w3-large w3-text-teal"></i>Father</p>
                    <p><i class="fa fa-envelope fa-fw w3-margin-right w3-large w3-text-teal"></i>jonathandoe@company.com.sg</p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96993220</p>

                </div>







                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-suitcase fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Co Curricular Activities</h2>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Boys Brigade</b></h5>
                    <p>Head</p>
                </div>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Life Sciences Club</b></h5>
                    <p>Member</p>
                    <hr>
                </div>


                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Teacher's Remarks</h2>
                    <div class="w3-container">
                        <p>Hardworking Student, soft spoken and shy</p>
                    </div>
                    <div class="w3-container">
                        <p>History of anxiety disorder, refrain from putting student on the spot</p>
                    </div>
                </div>



                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Injury History</h2>
                    <div class="w3-container">
                        <p>Chronic Bronchitis</p>
                    </div>
                    <div class="w3-container">
                        <p>Medial Collateral Ligament (MCL) injury history</p>
                        <hr>
                        <br>
                    </div>
                </div>

                <br>
                <!-- End Right Column -->
            </div>

            <!-- End Grid -->
        </div>

        <!-- End Page Container -->
    </div>

    <footer>
        <p>EduBuddy, Powered by<a href="https://www.w3schools.com/w3css/default.asp" target="_blank">w3.css</a></p>
    </footer>

</body>
</html>
```
###### \resources\StudentPage\Johnny Chen.html
``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Helvetica'>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">


<style>
html,body,h1,h2,h3,h4,h5,h6 {font-family: "Helvetica", sans-serif}
</style>
<body class="w3-light-grey">

<!-- Page Container -->
<div class="w3-content w3-margin-top" style="max-width:1400px;">

    <!-- The Grid -->
    <div class="w3-row-padding">

        <!-- Left Column -->
        <div class="w3-third">

            <div class="w3-white w3-text-grey w3-card-4">
                <div class="w3-display-container">
                    <img src="../docs/images/johnnychanjx.png" style="width:100%" alt="Avatar">

                </div>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>Johnny Chen</p>
                    <p><i class="fa fa-folder-o fa-fw w3-margin-right w3-large w3-text-teal"></i>S9191911F</p>
                    <p><i class="fa fa-home fa-fw w3-margin-right w3-large w3-text-teal"></i>10 Tampines North Street 3 Singapore 461110 </p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96992220</p>
                    <hr>



                    <p class="w3-large"><b><i class="fa fa-asterisk fa-fw w3-margin-right w3-text-teal"></i>Current Subjects</b></p>
                    <p>English</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:100%">A1</div>
                    </div>
                    <p>$subject2</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent2%">
                            <div class="w3-center w3-text-white">$grade2</div>
                        </div>
                    </div>
                    <p>$subject3</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent3%">$grade3</div>
                    </div>
                    <p>$subject4</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent4%">$grade4</div>
                    </div>
                    <p>$subject5</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent5%">$grade5</div>
                    </div>
                    <p>$subject6</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent6%">$grade6</div>
                    </div>

                    <hr>
                </div>
            </div><br>

            <!-- End Left Column -->
        </div>

        <!-- Right Column -->
        <div class="w3-twothird">

            <div class="w3-container w3-card w3-white w3-margin-bottom">



                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-address-card-o fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Next of Kin Details</h2>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>Jonathan Doe</p>
                    <p><i class="fa fa-genderless fa-fw w3-margin-right w3-large w3-text-teal"></i>Father</p>
                    <p><i class="fa fa-envelope fa-fw w3-margin-right w3-large w3-text-teal"></i>jonathandoe@company.com.sg</p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96993220</p>

                </div>







                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-suitcase fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Co Curricular Activities</h2>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Boys Brigade</b></h5>
                    <p>Head</p>
                </div>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Life Sciences Club</b></h5>
                    <p>Member</p>
                    <hr>
                </div>


                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Teacher's Remarks</h2>
                    <div class="w3-container">
                        <p>Hardworking Student, soft spoken and shy</p>
                    </div>
                    <div class="w3-container">
                        <p>History of anxiety disorder, refrain from putting student on the spot</p>
                    </div>
                </div>



                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Injury History</h2>
                    <div class="w3-container">
                        <p>Chronic Bronchitis</p>
                    </div>
                    <div class="w3-container">
                        <p>Medial Collateral Ligament (MCL) injury history</p>
                        <hr>
                        <br>
                    </div>
                </div>

                <br>
                <!-- End Right Column -->
            </div>

            <!-- End Grid -->
        </div>

        <!-- End Page Container -->
    </div>

    <footer>
        <p>EduBuddy, Powered by<a href="https://www.w3schools.com/w3css/default.asp" target="_blank">w3.css</a></p>
    </footer>

</body>
</html>
```
###### \resources\StudentPage\template.html
``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Helvetica'>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">


<style>
html,body,h1,h2,h3,h4,h5,h6 {font-family: "Helvetica", sans-serif}
</style>
<body class="w3-light-grey">

<!-- Page Container -->
<div class="w3-content w3-margin-top" style="max-width:1400px;">

    <!-- The Grid -->
    <div class="w3-row-padding">

        <!-- Left Column -->
        <div class="w3-third">

            <div class="w3-white w3-text-grey w3-card-4">
                <div class="w3-display-container">
                    <img src="../docs/images/johnnychanjx.png" style="width:100%" alt="Avatar">

                </div>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>$title</p>
                    <p><i class="fa fa-folder-o fa-fw w3-margin-right w3-large w3-text-teal"></i>$identityNumber</p>
                    <p><i class="fa fa-home fa-fw w3-margin-right w3-large w3-text-teal"></i>10 Tampines North Street 3 Singapore 461110 </p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96992220</p>
                    <hr>



                    <p class="w3-large"><b><i class="fa fa-asterisk fa-fw w3-margin-right w3-text-teal"></i>Current Subjects</b></p>
                    <p>$subject1</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent1%">$grade1</div>
                    </div>
                    <p>$subject2</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent2%">
                            <div class="w3-center w3-text-white">$grade2</div>
                        </div>
                    </div>
                    <p>$subject3</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent3%">$grade3</div>
                    </div>
                    <p>$subject4</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent4%">$grade4</div>
                    </div>
                    <p>$subject5</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent5%">$grade5</div>
                    </div>
                    <p>$subject6</p>
                    <div class="w3-light-grey w3-round-xlarge w3-small">
                        <div class="w3-container w3-center w3-round-xlarge w3-teal" style="width:$percent6%">$grade6</div>
                    </div>

                    <hr>
                </div>
            </div><br>

            <!-- End Left Column -->
        </div>

        <!-- Right Column -->
        <div class="w3-twothird">

            <div class="w3-container w3-card w3-white w3-margin-bottom">



                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-address-card-o fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Next of Kin Details</h2>
                <div class="w3-container">
                    <p><i class="fa fa-address-book fa-fw w3-margin-right w3-large w3-text-teal"></i>Jonathan Doe</p>
                    <p><i class="fa fa-genderless fa-fw w3-margin-right w3-large w3-text-teal"></i>Father</p>
                    <p><i class="fa fa-envelope fa-fw w3-margin-right w3-large w3-text-teal"></i>jonathandoe@company.com.sg</p>
                    <p><i class="fa fa-phone fa-fw w3-margin-right w3-large w3-text-teal"></i>+65 96993220</p>

                </div>







                <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-suitcase fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Co Curricular Activities</h2>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Boys Brigade</b></h5>
                    <p>Head</p>
                </div>
                <div class="w3-container">
                    <h5 class="w3-opacity"><b>Life Sciences Club</b></h5>
                    <p>Member</p>
                    <hr>
                </div>


                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Teacher's Remarks</h2>
                    <div class="w3-container">
                        <p>Hardworking Student, soft spoken and shy</p>
                    </div>
                    <div class="w3-container">
                        <p>History of anxiety disorder, refrain from putting student on the spot</p>
                    </div>
                </div>



                <div class="w3-container w3-card w3-white">
                    <h2 class="w3-text-grey w3-padding-16"><i class="fa fa-certificate fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Injury History</h2>
                    <div class="w3-container">
                        <p>Chronic Bronchitis</p>
                    </div>
                    <div class="w3-container">
                        <p>Medial Collateral Ligament (MCL) injury history</p>
                        <hr>
                        <br>
                    </div>
                </div>

                <br>
                <!-- End Right Column -->
            </div>

            <!-- End Grid -->
        </div>

        <!-- End Page Container -->
    </div>

    <footer>
        <p>EduBuddy, Powered by<a href="https://www.w3schools.com/w3css/default.asp" target="_blank">w3.css</a></p>
    </footer>

</body>
</html>
```
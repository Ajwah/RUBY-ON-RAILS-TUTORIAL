# Log of various errors whilst doing the book.

  ## A. git push heroku master
      **PROBLEM**: Push rejected, no Cedar-supported app detected HINT: This occurs when Heroku cannot detect the buildpack to use for this application automatically.
      
      **REASON**: Initialized git repo in root directory whereas it has to be app-directory.
      
      **SOLUTION**: 
      
                      1. rm -rf .git
                      
                      2. cd hello_app/
                      
                      3. git init
                      
                      4. git add . -A
                      
                      5. git commit -am "Reinitialize"
                      
                      6. heroku create --stack cedar
                      
                      7. git push heroku master
                      
      **SOURCE**: http://stackoverflow.com/questions/9305370/rails-3-2-heroku-push-rejected-no-cedar-supported-app-detected
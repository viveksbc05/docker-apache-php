node{
    stage("git staging and update"){
      sh """
        whoami
        echo "Updating to Latest"
        cd /home/vivek/fgv4/
        git pull origin development
 
       cd /home/vivek/fgv4/fairgate4/
       composer dump-autoload -a -o
       echo "Clearing Symfony cache `date`"
       cd /home/vivek/fgv4/fairgate4/
       php bin/console cache:clear --env=prod
       php bin/console cache:clear --env=dev
      """
    }
}

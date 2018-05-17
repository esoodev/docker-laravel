1. 
On UNIX :
docker run --rm -v $(pwd):/app composer install

On Windows :
docker run --rm -v ${pwd}:/app composer install

2. docker-compose exec app php artisan key:generate

The above command sends the artisan command to "app" container, which is defined in docker-compose.yml.
Here are some examples of other commands that may be used in development : 
    docker-compose exec app php artisan migrate --seed
    docker-compose exec app php artisan make:controller MyController
Pro Tip : create an alias like phpd that removes the need to type the full command, 
    eg: phpd artisan migrate --seed

3. docker-compose up 

4. Visit localhost:8080 on the browser!
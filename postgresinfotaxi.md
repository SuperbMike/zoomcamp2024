python ingest_data.py \    
    user= root \
    password  = root \
    host = localhost \
    port = 5433 \
    db = ny_taxi \
    table_name = yellow_taxi_trips \
    url=${URL}

URL = "https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz"

docker run taxi_ingest:v001 \
    python /app/ingest_data.py \
    --user root \
    --password=root \
    --host=localhost \
    --port=5433 \
    --db=ny_taxi \
    --table-name=yellow_taxi_trips \
    --url=https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz 
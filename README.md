# DBpedia_Spotlight for Ubuntu 16.04 (Dbpedia Spotlight, Entity linker easy setup )

Java setup
1. sudo add-apt-repository ppa:openjdk-r/ppa
2. sudo apt-get update
3. sudo apt-get install openjdk-8-jdk

Dbpedia Spotlight setup

1. wget http://downloads.dbpedia-spotlight.org/spotlight/dbpedia-spotlight-1.0.0.jar/download 
rename download file
2. mv download dbpedia-spotlight-1.0.0.jar
3. wget https://sourceforge.net/projects/dbpedia-spotlight/files/2016-10/en/model/en.tar.gz

4. tar xzf en.tar.gz

5. java -jar dbpedia-spotlight-1.0.0.jar en http://localhost:2222/rest

Test the server:
curl http://localhost:2222/rest/annotate \
  -H "Accept: text/xml" \
  --data-urlencode "text=Brazilian state-run giant oil company Petrobras signed a three-year technology and research cooperation agreement with oil service provider Halliburton." \
  --data "confidence=0" \
  --data "support=0"

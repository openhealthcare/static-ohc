PROJ = "eLCID"

task :build do
  p "Building OHC Static Site"
  sh "rm -rf _build"
  sh "rm -rf dist"
  sh "jekyll build"
  sh "cp -rva _site _build"
  sh "mv _build/index.html _build/stat_index.html"
  sh "mkdir dist"
  sh "cd _build/&& tar zcvf static.ohc.tar.gz *"
  sh "mv _build/static.ohc.tar.gz dist/"
end

task :deploy do
  p "Deploying OHC Static Site"
  sh "scp dist/static.ohc.tar.gz openhealthcare.org.uk:/tmp/"
  sh 'ssh openhealthcare.org.uk "cd /var/altwww/new_ohc; tar zxvf /tmp/static.ohc.tar.gz --overwrite"'
end

task :hackit => [:build, :deploy] do
end

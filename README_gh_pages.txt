cp -R slm_glacial_srtm slm_glacial_srtm_pages
cd slm_glacial_srtm_pages
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index 
git clean -fdx
cp -R ../tmp_pages/* .
vi _config.yml 
git add .; git commit -m "Create gh-pages branch for web front-end"
git push --set-upstream origin gh-pages

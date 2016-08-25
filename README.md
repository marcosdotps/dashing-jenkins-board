To run this, download this development at ${WORKSPACE}

docker rm -f dashing && docker run -v ${WORKSPACE}/dashing-widgets/jenkinsJob/:/jobs -v ${WORKSPACE}/dashing-widgets/dashboard:/dashboards -e GEMS="httparty jsonpath" -d -p 8080:3030 --name dashing frvi/dashing && docker logs -f dashing

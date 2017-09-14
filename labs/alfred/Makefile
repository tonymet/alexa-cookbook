PROFILE=sotion.tonym
FUNCTION=alfredRideFunction
dist/lambda.zip: src/*
	cp src/* dist; \
	cp -R node_modules dist/ ; \
	cd dist ; \
	zip -r lambda.zip *
deploy: dist/lambda.zip
	aws --profile=${PROFILE} lambda update-function-code --function-name ${FUNCTION} --zip-file fileb://dist/lambda.zip


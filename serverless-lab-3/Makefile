.PHONY: build clean deploy

build:
	env GOARCH=amd64 GOOS=linux CGO_ENABLED=0 go build -ldflags="-s -w" -o bin/create create/main.go 
	

clean:
	rm -rf ./bin

deploy: clean build
	sls deploy --verbose

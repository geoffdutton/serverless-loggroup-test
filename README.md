## Serverless 1.5.1 Error

Using serverless 1.5.1:
```
npm install serverless@1.5.1 -g
```

Then:
```
sls deploy --verbose
```

Will throw an error that says:

```
  Serverless Error ---------------------------------------
 
     An error occurred while provisioning your stack: IamPolicyLambdaExecution
     - Template error: LogGroup /aws/lambda/loggroup-test-dev-checkSomething
     doesn't exist.
 
  Get Support --------------------------------------------
     Docs:          docs.serverless.com
     Bugs:          github.com/serverless/serverless/issues
 
  Your Environment Information -----------------------------
     OS:                 darwin
     Node Version:       4.5.0
     Serverless Version: 1.5.1
```

If you comment out:

```$xslt
#  ab:
#    handler: handler.b
```

It works...

If change the function name:

```
  b:
    handler: handler.b
```

It works...
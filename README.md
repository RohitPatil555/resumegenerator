# resumegenerator
This help you to generate resume from markdown to html.
And then you can use browser to save page as pdf to share across other via mail.
It will save a lot of time in formating resume whenever you try to add material or remove from resume.

This take resume contain in markdown language and then convert them into html page.
It have sample as per my formating style but you can customize and use tool to install same.

# Prerequired

* Install python3-pip.
* Install markdown and jinja python module.

# Example

* I have create "data" folder for example.
```
├── bin
│   └── resumegenerator
├── data
│   ├── config.json
│   ├── resume
│   │   ├── test0.md
│   │   ├── test10.md
│   │   ├── test1.md
│   │   ├── test2.md
│   │   ├── test3_0.md
│   │   ├── test3_1.md
│   │   └── test4.md
│   ├── style
│   │   └── base.css
│   └── tmpls
│       └── resume.tmpl
└── output
    └── resumetest.html
```
* resume format have various section e.g. summary, skill, experience, education etc.
* And all this section are cature in respective files test1, test2, test3_* , test4 etc.
* HTML page template is present in folder "tmpls/resume.tmpl" 
* And resume formating can be done via "style/base.css".
* Config file example as shown below :
```
{
  "folder":"resume",
  "stylesheet" : "style/base.css",
  "templatefile" : "tmpls/resume.tmpl",
  "header" : "test0.md",
  "footer" : "test10.md",
  "summary": "test1.md",
  "skills" : "test2.md",
  "education" : "test4.md",
  "experiences": [
    "test3_0.md",
    "test3_1.md"
  ]
}
```

* Execute resume generator tool as shown below.
```
./bin/resumegenerator -c data/config.json -o ../output/resumetest.html
```

* I have also added sample html file view.

# Introduction

Two files are created in the current working directory when running `jmeter` command to open the test plan GUI editor.

* YOUR-TEST-PLAN.jmx
* jmeter.log

---

To open English version GUI editor

```
export JVM_ARGS="-Duser.language=en -Duser.region=EN"
jmeter
```

---

To open an existing test plan, run `jmeter -t YOUR-TEST-PLAN.jmx`

---

To run an existing test plan in non-GUI mode, run `jmeter -t YOUR-TEST-PLAN.jmx -n -l reports.jtl`

Results are appended in the file `reports.jtl` if running multiple times.

If the property jmeterengine.stopfail.system.exit is set to true (default is false), then JMeter will invoke System.exit(1) if it cannot stop all threads. Normally this is not necessary.

To change the property jmeterengine.stopfail.system.exit, use one of these methods:

* \<JMETER INSTALLATION\>/jmeter.properties
* \<JMETER INSTALLATION\>/user.properties (override jmeter.properties)
* jmeter -Jjmeterengine.stopfail.system.exit=true ... (override user.properties)

\<JMETER INSTALLATION> e.g., /usr/local/Cellar/jmeter/2.13/libexec/bin in my case.

---

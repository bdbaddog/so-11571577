Import("env")

env = env.Clone(FOOLIBDIR=Dir("foolib"))
subdirs=["barexec", "foolib"]
SConscript(dirs=subdirs, exports=["env"])

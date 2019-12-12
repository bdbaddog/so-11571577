# Common environment for all build modes.
common = Environment(CCFLAGS=["-Wall"], CPPPATH=["#foolib/inc"])

# Build-mode specific environments.
debug = common.Clone()
debug.Append(CCFLAGS=["-O0"])
release = common.Clone()
release.Append(CCFLAGS=["-O"], CPPDEFINES=["NDEBUG"])

# Run all builds.
SConscript("SConscript", exports={"env": debug}, variant_dir="debug")
SConscript("SConscript", exports={"env": release}, variant_dir="release")
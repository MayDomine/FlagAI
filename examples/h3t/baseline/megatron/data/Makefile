CXXFLAGS += -O3 -Wall -shared -std=c++11 -fPIC -fdiagnostics-color # -I/root/miniconda3/envs/pytorch/include/python3.9
CPPFLAGS += $(shell python3 -m pybind11 --includes)
LIBNAME = helpers
LIBEXT = $(shell python3-config --extension-suffix)

default: $(LIBNAME)$(LIBEXT)

%$(LIBEXT): %.cpp
	$(CXX) $(CXXFLAGS) $(CPPFLAGS) $< -o $@

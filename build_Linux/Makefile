# -*- Makefile -*-

arch = Linux_MPI
setup_file = setup/Make.$(arch)

include $(setup_file)


HPCG_DEPS = src/CG.o \
	    src/CG_ref.o \
	    src/TestCG.o \
	    src/ComputeResidual.o \
	    src/ExchangeHalo.o \
	    src/GenerateGeometry.o \
	    src/GenerateProblem.o \
	    src/GenerateProblem_ref.o \
	    src/CheckProblem.o \
	    src/MixedBaseCounter.o \
	    src/OptimizeProblem.o \
	    src/ReadHpcgDat.o \
	    src/ReportResults.o \
	    src/SetupHalo.o \
	    src/SetupHalo_ref.o \
	    src/TestSymmetry.o \
	    src/TestNorms.o \
	    src/WriteProblem.o \
	    src/YAML_Doc.o \
	    src/YAML_Element.o \
	    src/ComputeDotProduct.o \
	    src/ComputeDotProduct_ref.o \
	    src/mytimer.o \
	    src/ComputeOptimalShapeXYZ.o \
	    src/ComputeSPMV.o \
	    src/ComputeSPMV_ref.o \
	    src/ComputeSYMGS.o \
	    src/ComputeSYMGS_ref.o \
	    src/ComputeWAXPBY.o \
	    src/ComputeWAXPBY_ref.o \
	    src/ComputeMG_ref.o \
	    src/ComputeMG.o \
	    src/ComputeProlongation_ref.o \
	    src/ComputeRestriction_ref.o \
	    src/CheckAspectRatio.o \
	    src/OutputFile.o \
	    src/GenerateCoarseProblem.o \
	    src/init.o \
	    src/finalize.o

# These header files are included in many source files, so we recompile every file if one or more of these header is modified.
PRIMARY_HEADERS = /ihome/me2054/pea11/hpcg/src/Geometry.hpp /ihome/me2054/pea11/hpcg/src/SparseMatrix.hpp /ihome/me2054/pea11/hpcg/src/Vector.hpp /ihome/me2054/pea11/hpcg/src/CGData.hpp \
                  /ihome/me2054/pea11/hpcg/src/MGData.hpp /ihome/me2054/pea11/hpcg/src/hpcg.hpp

all: bin/xhpcg

bin/xhpcg: src/main.o $(HPCG_DEPS)
	$(LINKER) $(LINKFLAGS) src/main.o $(HPCG_DEPS) $(HPCG_LIBS) -o bin/xhpcg

clean:
	rm -f src/*.o bin/xhpcg

.PHONY: all clean

src/main.o: /ihome/me2054/pea11/hpcg/src/main.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/CG.o: /ihome/me2054/pea11/hpcg/src/CG.cpp /ihome/me2054/pea11/hpcg/src/CG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/CG_ref.o: /ihome/me2054/pea11/hpcg/src/CG_ref.cpp /ihome/me2054/pea11/hpcg/src/CG_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/TestCG.o: /ihome/me2054/pea11/hpcg/src/TestCG.cpp /ihome/me2054/pea11/hpcg/src/TestCG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeResidual.o: /ihome/me2054/pea11/hpcg/src/ComputeResidual.cpp /ihome/me2054/pea11/hpcg/src/ComputeResidual.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ExchangeHalo.o: /ihome/me2054/pea11/hpcg/src/ExchangeHalo.cpp /ihome/me2054/pea11/hpcg/src/ExchangeHalo.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/GenerateGeometry.o: /ihome/me2054/pea11/hpcg/src/GenerateGeometry.cpp /ihome/me2054/pea11/hpcg/src/GenerateGeometry.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/GenerateProblem.o: /ihome/me2054/pea11/hpcg/src/GenerateProblem.cpp /ihome/me2054/pea11/hpcg/src/GenerateProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/GenerateProblem_ref.o: /ihome/me2054/pea11/hpcg/src/GenerateProblem_ref.cpp /ihome/me2054/pea11/hpcg/src/GenerateProblem_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/CheckProblem.o: /ihome/me2054/pea11/hpcg/src/CheckProblem.cpp /ihome/me2054/pea11/hpcg/src/CheckProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/MixedBaseCounter.o: /ihome/me2054/pea11/hpcg/src/MixedBaseCounter.cpp /ihome/me2054/pea11/hpcg/src/MixedBaseCounter.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/OptimizeProblem.o: /ihome/me2054/pea11/hpcg/src/OptimizeProblem.cpp /ihome/me2054/pea11/hpcg/src/OptimizeProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ReadHpcgDat.o: /ihome/me2054/pea11/hpcg/src/ReadHpcgDat.cpp /ihome/me2054/pea11/hpcg/src/ReadHpcgDat.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ReportResults.o: /ihome/me2054/pea11/hpcg/src/ReportResults.cpp /ihome/me2054/pea11/hpcg/src/ReportResults.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/SetupHalo.o: /ihome/me2054/pea11/hpcg/src/SetupHalo.cpp /ihome/me2054/pea11/hpcg/src/SetupHalo.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/SetupHalo_ref.o: /ihome/me2054/pea11/hpcg/src/SetupHalo_ref.cpp /ihome/me2054/pea11/hpcg/src/SetupHalo_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/TestSymmetry.o: /ihome/me2054/pea11/hpcg/src/TestSymmetry.cpp /ihome/me2054/pea11/hpcg/src/TestSymmetry.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/TestNorms.o: /ihome/me2054/pea11/hpcg/src/TestNorms.cpp /ihome/me2054/pea11/hpcg/src/TestNorms.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/WriteProblem.o: /ihome/me2054/pea11/hpcg/src/WriteProblem.cpp /ihome/me2054/pea11/hpcg/src/WriteProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/YAML_Doc.o: /ihome/me2054/pea11/hpcg/src/YAML_Doc.cpp /ihome/me2054/pea11/hpcg/src/YAML_Doc.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/YAML_Element.o: /ihome/me2054/pea11/hpcg/src/YAML_Element.cpp /ihome/me2054/pea11/hpcg/src/YAML_Element.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeDotProduct.o: /ihome/me2054/pea11/hpcg/src/ComputeDotProduct.cpp /ihome/me2054/pea11/hpcg/src/ComputeDotProduct.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeDotProduct_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeDotProduct_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeDotProduct_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/finalize.o: /ihome/me2054/pea11/hpcg/src/finalize.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/init.o: /ihome/me2054/pea11/hpcg/src/init.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/mytimer.o: /ihome/me2054/pea11/hpcg/src/mytimer.cpp /ihome/me2054/pea11/hpcg/src/mytimer.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeOptimalShapeXYZ.o: /ihome/me2054/pea11/hpcg/src/ComputeOptimalShapeXYZ.cpp /ihome/me2054/pea11/hpcg/src/ComputeOptimalShapeXYZ.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeSPMV.o: /ihome/me2054/pea11/hpcg/src/ComputeSPMV.cpp /ihome/me2054/pea11/hpcg/src/ComputeSPMV.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeSPMV_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeSPMV_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeSPMV_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeSYMGS.o: /ihome/me2054/pea11/hpcg/src/ComputeSYMGS.cpp /ihome/me2054/pea11/hpcg/src/ComputeSYMGS.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeSYMGS_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeSYMGS_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeSYMGS_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeWAXPBY.o: /ihome/me2054/pea11/hpcg/src/ComputeWAXPBY.cpp /ihome/me2054/pea11/hpcg/src/ComputeWAXPBY.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeWAXPBY_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeWAXPBY_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeWAXPBY_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeMG_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeMG_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeMG_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeMG.o: /ihome/me2054/pea11/hpcg/src/ComputeMG.cpp /ihome/me2054/pea11/hpcg/src/ComputeMG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeProlongation_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeProlongation_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeProlongation_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/ComputeRestriction_ref.o: /ihome/me2054/pea11/hpcg/src/ComputeRestriction_ref.cpp /ihome/me2054/pea11/hpcg/src/ComputeRestriction_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/GenerateCoarseProblem.o: /ihome/me2054/pea11/hpcg/src/GenerateCoarseProblem.cpp /ihome/me2054/pea11/hpcg/src/GenerateCoarseProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/CheckAspectRatio.o: /ihome/me2054/pea11/hpcg/src/CheckAspectRatio.cpp /ihome/me2054/pea11/hpcg/src/CheckAspectRatio.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@

src/OutputFile.o: /ihome/me2054/pea11/hpcg/src/OutputFile.cpp /ihome/me2054/pea11/hpcg/src/OutputFile.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/ihome/me2054/pea11/hpcg/src $< -o $@


BASENAME = hamid

SOURCES = $(BASENAME).tex \
	glossary.tex \
	intro.tex \
	biblio.tex \
	aadlrs.tex \
	code_gen.tex \
	adv_gen.tex \
	formal_sem.tex \
	conclusions.tex \
	mcc.tex \
	ada.tex \
	french_summary.tex \
	thenst.cls \
	thenst.sty \
	Makefile

BIBLIOGRAPHY = $(BASENAME).bib

FIGS = figs/det_breach_nobreach.eps \
	figs/hard_vs_soft.eps \
	figs/rt_apps_overview.eps \
	figs/aadl_ex.eps \
	figs/ARC_process.eps \
	figs/block_diag.eps \
	figs/caseStudy.eps \
	figs/composed.eps \
	figs/dataports.eps \
	figs/det_breach1.eps \
	figs/det_breach.eps \
	figs/det.eps \
	figs/det_no_breach.eps \
	figs/eventports.eps \
	figs/fourone_b.eps \
	figs/impulse.eps \
	figs/protocol_task.eps \
	figs/stagger2.eps \
	figs/stagger.eps \
	figs/stepper2.eps \
	figs/stepper_DBX.eps \
	figs/stepper_DBX_vect.eps \
	figs/stepper.eps \
	figs/thread2task.eps \
	figs/transform.eps \
	figs/sporadic_caveat.eps \
	figs/process.eps \
	figs/osate_arch.eps \
	figs/comp_code.eps \
	figs/conn_semantics.eps \
	figs/modes.eps \
	figs/cyclic_exec.eps \
	figs/thread_timeline.eps \
	figs/precedence_priority.eps \
	figs/precedence_offset.eps \
	figs/tasking_config2.eps \
	figs/tasking_config.eps \
	figs/example.eps \
	figs/rmm_inst.eps \
	figs/GAP_sys_arch.eps \
	figs/mode_periodic.eps \
	figs/mof.eps \
	figs/scade_eq.eps \
	figs/mde_chain.eps \
	figs/class.eps \
	figs/class_diag.eps \
	figs/inherited_rate_scope.eps \
	figs/step_down_scope.eps \
	figs/abs_simulink.eps \
	figs/abs_block_simulink.eps \
	figs/subsystem_simulink.eps \
	figs/subsystem_rate_cmp_simulink.eps \
	figs/statechart.eps \
	figs/dataports_fanout.eps \
	figs/axes.eps \
	figs/aoa.eps \
	figs/synchronizer.eps \
	figs/rmm.eps \
	figs/rate_transition.eps \
	figs/protocol2.eps \
	figs/ex1.eps \
	figs/control.eps \
	figs/control_simple.eps \
	figs/control_simple_breach.eps \
	figs/control_simple_nobreach.eps \
	figs/lotos_lts_ex1.eps \
	figs/ho-exch.eps \
	figs/ho-example.eps \
	figs/second_order.eps \
	figs/stepper_code.eps \
	figs/lotos_proc_code.eps \
	figs/sync_transform.eps \
	figs/logo_enst.eps \
	figs/logo_edite.eps \

PDFFIGS = figs/det_breach_nobreach.pdf \
	figs/hard_vs_soft.pdf \
	figs/rt_apps_overview.pdf \
	figs/aadl_ex.pdf \
	figs/ARC_process.pdf \
	figs/block_diag.pdf \
	figs/caseStudy.pdf \
	figs/composed.pdf \
	figs/dataflow.pdf \
	figs/dataports.pdf \
	figs/det_breach1.pdf \
	figs/det_breach.pdf \
	figs/det.pdf \
	figs/det_no_breach.pdf \
	figs/eventports.pdf \
	figs/fourone_b.pdf \
	figs/impulse.pdf \
	figs/protocol_task.pdf \
	figs/stagger2.pdf \
	figs/stagger.pdf \
	figs/stepper2.pdf \
	figs/stepper_DBX.pdf \
	figs/stepper_DBX_vect.pdf \
	figs/stepper.pdf \
	figs/thread2task.pdf \
	figs/transform.pdf \
	figs/sporadic_caveat.pdf \
	figs/process.pdf \
	figs/osate_arch.pdf \
	figs/comp_code.pdf \
	figs/conn_semantics.pdf \
	figs/modes.pdf \
	figs/cyclic_exec.pdf \
	figs/thread_timeline.pdf \
	figs/precedence_priority.pdf \
	figs/precedence_offset.pdf \
	figs/tasking_config2.pdf \
	figs/tasking_config.pdf \
	figs/example.pdf \
	figs/rmm_inst.pdf \
	figs/GAP_sys_arch.pdf \
	figs/mode_periodic.pdf \
	figs/mof.pdf \
	figs/scade_eq.pdf \
	figs/mde_chain.pdf \
	figs/class.pdf \
	figs/class_diag.pdf \
	figs/inherited_rate_scope.pdf \
	figs/step_down_scope.pdf \
	figs/abs_simulink.pdf \
	figs/abs_block_simulink.pdf \
	figs/subsystem_simulink.pdf \
	figs/subsystem_rate_cmp_simulink.pdf \
	figs/statechart.pdf \
	figs/dataports_fanout.pdf \
	figs/axes.pdf \
	figs/aoa.pdf \
	figs/synchronizer.pdf \
	figs/rmm.pdf \
	figs/rate_transition.pdf \
	figs/protocol2.pdf \
	figs/ex1.pdf \
	figs/control_simple.pdf \
	figs/control.pdf \
	figs/control_simple_breach.pdf \
	figs/control_simple_nobreach.pdf \
	figs/lotos_lts_ex1.pdf \
	figs/ho-exch.pdf \
	figs/ho-example.pdf \
	figs/second_order.pdf \
	figs/stepper_code.pdf \
	figs/lotos_proc_code.pdf \
	figs/sync_transform.pdf \
	figs/logo_enst.pdf \
	figs/logo_edite.pdf
#	figs/execComparison.pdf \

all: $(BASENAME).dvi

pdf: $(BASENAME).pdf

ps: $(BASENAME).ps

dvi: $(BASENAME).dvi

$(BASENAME).dvi: $(SOURCES) $(FIGS) $(BIBLIOGRAPHY)
	latex $(BASENAME).tex
	bibtex $(BASENAME)
	latex $(BASENAME).tex
	latex $(BASENAME).tex

$(BASENAME).pdf: $(SOURCES) $(PDFFIGS) $(BIBLIOGRAPHY)
	pdflatex $(BASENAME).tex
	bibtex $(BASENAME)
	pdflatex $(BASENAME).tex
	pdflatex $(BASENAME).tex

$(BASENAME).ps: $(BASENAME).dvi
	dvips -o $(BASENAME).ps $(BASENAME).dvi

%.eps: %.svg
	inkscape -z --export-text-to-path --export-eps=$@ -f=$<

%.pdf: %.eps
	ps2pdf -dEPSCrop $< $@

cleanbib:
	rm -rf *.aux *.log *~ *.bbl *.blg *.bak *#* *.lof *.lot *.toc

clean:
	rm -rf *.aux *.log *.dvi *.ps *.pdf *~ *.bbl *.blg *.bak *#* *.lof *.lot *.toc

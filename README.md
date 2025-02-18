MCMC_KVLCC2.ipynbでMCMCを実行して微係数サンプルを作成
simulation.ipynbでMPC用の外乱あり観測データを作成
MPC_KVLCC2.ipynbで~/MCMC/resultの微係数のcsvと、~/MPC/observationの観測データのcsvを参照してMPCを実行

使用パッケージ
using DifferentialEquations, Interpolations, ParameterizedFunctions, Turing, ForwardDiff, JuMP, Ipopt, ProgressMeter
using DataFrames, CSV, Random, Revise, Dierckx, Distributions, Parameters, PyPlot, PyCall, LaTeXStrings
using KernelDensity: kde
@pyimport numpy as np
@pyimport scienceplot

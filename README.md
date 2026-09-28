# llama-locally-windows

1. go to  https://github.com/ggml-org/llama.cpp/releases
2. download choose your cuda ( check with nvidia-smi)
   - Windows x64 (CUDA 12) - CUDA 12.4 DLLs
   - Windows x64 (CUDA 13) - CUDA 13.4 DLLs
3. extract file form llama-b11223-bin-win-cuda-13.4-x64.zip  first  and follow cudart-llama-bin-win-cuda-13.4-x64.zip  (into  llama-b11223-bin-win-cuda-13.4-x64 folder )
4. create folder inside folder llama-b11223-bin-win-cuda-13.4-x64   `` mkdir model ``
5. download model (.GGUF)  past file into   llama-b11223-bin-win-cuda-13.4-x64/model
6. start server
   `` llama-server.exe -m models\Your-Model.gguf -ngl 99 -c 8192 --host 127.0.0.1 --port 8080 --flash-attn --jinja --temp 0.6 --top-p 0.95 --top-k 20 ``

7. open browser 127.0.0.1:8080 

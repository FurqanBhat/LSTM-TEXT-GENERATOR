# LSTM-TEXT-GENERATOR

#  Custom LSTM from Scratch – Shakespeare Text Generator

This project demonstrates a character-level text generation model trained on Shakespeare's writings using PyTorch. It explores two custom implementations of the Long Short-Term Memory (LSTM) network:

1. **Traditional LSTM** — Follows the standard gate architecture.
2. **NEWLSTM** — A simplified variation where the input gate is approximated as `1 - forget_gate`.

---

##  Highlights

- Built LSTM **from scratch** without using PyTorch’s built-in `nn.LSTM`.
- Created a character-level **text generator**.
- Compared performance of **standard LSTM** vs. **NEWLSTM** design.
- Trained on a small dataset: `shakespeare_100.txt`.

---

##  Architecture

###  Traditional LSTM
Implements standard gating:
- Forget gate
- Input gate
- Cell gate
- Output gate

###  NEWLSTM
Simplified variant:
- No explicit input gate
- `input_gate = 1 - forget_gate`
- Reduced parameter count and slightly faster training

---

##  Training Results

| Model         | Final Loss | Training Time |
|---------------|------------|----------------|
| Traditional LSTM | **0.0807** | 256.56 seconds |
| NEWLSTM          | **0.0743** | 207.55 seconds |

Both models converge well. NEWLSTM trains faster and still achieves comparable (or slightly better) performance.

---



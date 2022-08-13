---
title: "Say hello to Doks 👋"
description: "Introducing Doks, a Hugo theme helping you build modern documentation websites that are secure, fast, and SEO-ready — by default."
excerpt: "Introducing Doks, a Hugo theme helping you build modern documentation websites that are secure, fast, and SEO-ready — by default."
date: 2020-11-04T09:19:42+01:00
lastmod: 2020-11-04T09:19:42+01:00
draft: false
weight: 50
images: []
categories: ["News"]
tags: ["security", "performance", "SEO"]
contributors: ["Henk Verlinde"]
pinned: false
homepage: false
---

# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`class `[`DnnGop`](#class_dnn_gop) | 
`class `[`PronDecoder`](#class_pron_decoder) | 
`class `[`Scorer`](#class_scorer) | 
`class `[`ScorerKR`](#class_scorer_k_r) | 
`class `[`ScorerUK`](#class_scorer_u_k) | 
`class `[`ScorerUS`](#class_scorer_u_s) | 
`class `[`Scoring`](#class_scoring) | 
`struct `[`__stFLUENCY_GROUP`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p) | 
`struct `[`__stLABEL`](#struct____st_l_a_b_e_l) | 
`struct `[`__stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m) | 
`struct `[`__stSENTENCE_ITEM`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m) | 
`struct `[`__stSYLL_LETTER_ITEM`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m) | 
`struct `[`__stSYLL_PHONE_ITEM`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m) | 
`struct `[`__stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m) | 
`struct `[`ASRContext`](#struct_a_s_r_context) | 
`struct `[`ASRSession`](#struct_a_s_r_session) | 
`struct `[`ScoringConfig`](#struct_scoring_config) | 

# class `DnnGop` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`DnnGop`](#class_dnn_gop_1affbe61f9d16a917eed7dfa780feb3d97)`()` | 
`public virtual  `[`~DnnGop`](#class_dnn_gop_1a5b5c1363c5940de7128851a4b432847e)`()` | 
`public void `[`Init`](#class_dnn_gop_1aa6cee38bd0af6a3c0c192455cc7477c4)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext)` | 
`public void `[`Compute`](#class_dnn_gop_1a8e0680973b47ebc5fa4900ac13d97fb9)`(fst::VectorFst< fst::StdArc > * pLexFst,const kaldi::CuMatrix< kaldi::BaseFloat > & feature,const std::vector< int32_t > & vtTranscript,kaldi::BaseFloat fScaleTransition,kaldi::BaseFloat fScaleAcoustic,kaldi::BaseFloat fScaleSelfLoop)` | 
`public inline void `[`get_phones_item`](#class_dnn_gop_1afa033538d618ef4fa8a87636377ce73c)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_item)` | 

## Members

#### `public  `[`DnnGop`](#class_dnn_gop_1affbe61f9d16a917eed7dfa780feb3d97)`()` 

#### `public virtual  `[`~DnnGop`](#class_dnn_gop_1a5b5c1363c5940de7128851a4b432847e)`()` 

#### `public void `[`Init`](#class_dnn_gop_1aa6cee38bd0af6a3c0c192455cc7477c4)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext)` 

#### `public void `[`Compute`](#class_dnn_gop_1a8e0680973b47ebc5fa4900ac13d97fb9)`(fst::VectorFst< fst::StdArc > * pLexFst,const kaldi::CuMatrix< kaldi::BaseFloat > & feature,const std::vector< int32_t > & vtTranscript,kaldi::BaseFloat fScaleTransition,kaldi::BaseFloat fScaleAcoustic,kaldi::BaseFloat fScaleSelfLoop)` 

#### `public inline void `[`get_phones_item`](#class_dnn_gop_1afa033538d618ef4fa8a87636377ce73c)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_item)` 

# class `PronDecoder` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`PronDecoder`](#class_pron_decoder_1a56fee758d09b82be2bc1e597a76bb78d)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext)` | 
`public  `[`~PronDecoder`](#class_pron_decoder_1a7ed80425223297b7ace8aea157426221)`()` | 
`public void `[`set_ref_text`](#class_pron_decoder_1a4df5f70750d79a044b9d8c4c9333ce87)`(void * pLexFst,const char * pszRefText,const char * pszSyllPhn,const char * pszSyllLtr,const char * pszRefPathName)` | 
`public void `[`add_pcm_block`](#class_pron_decoder_1a910de8113ed495b2ccc3cd43b9b927b2)`(const char * buffer,unsigned long buffer_length)` | 
`public void `[`decode`](#class_pron_decoder_1a307c4293631e8025023d662e7fec0dcc)`()` | 
`public void `[`decode_audio`](#class_pron_decoder_1a0a7ec6a26dc919fb1aa321f7011b38c7)`(const char * buffer,unsigned long buffer_length)` | 
`public void `[`decode_pcm`](#class_pron_decoder_1a98fbada9c897acd98debd8e877a4330b)`(std::string filename)` | 
`public void `[`decode_wav`](#class_pron_decoder_1a2cfc9c164f5732128f19670fe3954bd6)`(std::string filename)` | 
`public inline std::string & `[`get_score`](#class_pron_decoder_1a483bb684ceef037818ed6870e73e0c15)`()` | 

## Members

#### `public  `[`PronDecoder`](#class_pron_decoder_1a56fee758d09b82be2bc1e597a76bb78d)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext)` 

#### `public  `[`~PronDecoder`](#class_pron_decoder_1a7ed80425223297b7ace8aea157426221)`()` 

#### `public void `[`set_ref_text`](#class_pron_decoder_1a4df5f70750d79a044b9d8c4c9333ce87)`(void * pLexFst,const char * pszRefText,const char * pszSyllPhn,const char * pszSyllLtr,const char * pszRefPathName)` 

#### `public void `[`add_pcm_block`](#class_pron_decoder_1a910de8113ed495b2ccc3cd43b9b927b2)`(const char * buffer,unsigned long buffer_length)` 

#### `public void `[`decode`](#class_pron_decoder_1a307c4293631e8025023d662e7fec0dcc)`()` 

#### `public void `[`decode_audio`](#class_pron_decoder_1a0a7ec6a26dc919fb1aa321f7011b38c7)`(const char * buffer,unsigned long buffer_length)` 

#### `public void `[`decode_pcm`](#class_pron_decoder_1a98fbada9c897acd98debd8e877a4330b)`(std::string filename)` 

#### `public void `[`decode_wav`](#class_pron_decoder_1a2cfc9c164f5732128f19670fe3954bd6)`(std::string filename)` 

#### `public inline std::string & `[`get_score`](#class_pron_decoder_1a483bb684ceef037818ed6870e73e0c15)`()` 

# class `Scorer` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline  `[`Scorer`](#class_scorer_1a78a058b089bea56c1f1f97fa1981806b)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` | 
`public inline virtual  `[`~Scorer`](#class_scorer_1a327de016aeef0e88858c6a99acb4da28)`()` | 
`public void `[`SetPhoneItem`](#class_scorer_1a14423461af8429095721a7f1ede040e6)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phone_items)` | 
`public void `[`SetPhoneRefItem`](#class_scorer_1ab607b509878f65be3ac2967a46d5e720)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_ref_items)` | 
`public void `[`SetWordItem`](#class_scorer_1a34adbb8d192a3fb7f60619987a5ce8dc)`(std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > & word_items)` | 
`public void `[`DoPhoneScoring`](#class_scorer_1aaa69d47fd2799d9b79d13b04b11ddfd3)`()` | 
`public void `[`DoWordScoring`](#class_scorer_1ae1b65cdf255080b24bb638d08a75539b)`()` | 
`public void `[`DoSyllabification`](#class_scorer_1a32574dce8fe3d75c2c3a7084be9395ed)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` | 
`public void `[`DoFluency_v2`](#class_scorer_1a28567753ed960618eafaad21e5329ed6)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` | 
`public std::string `[`GetResult`](#class_scorer_1a32c9ac75e8a8b45d11cc0a9dac22f83b)`(std::vector< std::vector< std::string > > & vt_word_sentence)` | 
`protected `[`ASRContext`](#struct_a_s_r_context)` * `[`m_pASRContext`](#class_scorer_1a735cfb3798b1f6c4f385cdd49089faec) | 
`protected ScoreSettings * `[`m_pScoreSettings`](#class_scorer_1a9f75f61238f7e360aa733da6067228a9) | 
`protected std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > `[`phone_items_`](#class_scorer_1afad57f1dd4807e9c5417b03c4f9087b3) | 
`protected std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > `[`phone_ref_items_`](#class_scorer_1af00cc35a3e2ea75ce25424f89913d18d) | 
`protected std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > `[`word_items_`](#class_scorer_1a57b6d100cddaff98e5cd7c13b68b841c) | 
`protected std::vector< `[`stSENTENCE_ITEM`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m)` > `[`sentence_items_`](#class_scorer_1a4e7aaa2a3f49ced1ef79d1d442f9ece0) | 
`protected std::stringstream `[`result_stream_`](#class_scorer_1a10cb999d477b7508dfa507348d0e1cee) | 
`protected size_t `[`phone_index_`](#class_scorer_1a56689342445ad7d6327a4990c809c8c4) | 
`protected rapidjson::Document `[`document_`](#class_scorer_1ab738343606b987a6073982f0bbe00d9d) | 
`protected size_t `[`sil_phone_count_`](#class_scorer_1a39d8e0ccd909cefc32ee3a3bbc7f3834) | 
`protected size_t `[`sil_between_sentences_count_`](#class_scorer_1a1f7102e65168ef8d25c9b46745dd5671) | 
`protected size_t `[`sil_between_words_count_`](#class_scorer_1aea7d59c796301f691a0fdc6092b62edc) | 
`protected double `[`sil_between_sentence_score_`](#class_scorer_1aa8873740ee04da08e0cad7bc3198381a) | 
`protected std::vector< double > `[`sil_within_sentence_score_`](#class_scorer_1aa1c67b7c50577658240a987e3816d932) | 
`protected std::vector< std::string > `[`m_vtConsonants`](#class_scorer_1a1a8b024c50241cba1d887f6717046ac7) | 
`protected std::vector< std::string > `[`m_vtVowels`](#class_scorer_1a949a9e4eedd29939df7ed5610dae8a1c) | 
`protected std::vector< std::string > `[`m_vtOnsets`](#class_scorer_1a857150f08a4ce2a500fbdd239d8026b2) | 
`protected std::vector< std::string > `[`m_vtPauses`](#class_scorer_1a617d0c3fd99aa1c73aa6b8782be6196c) | 
`protected std::vector< `[`stFLUENCY_GROUP`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p)` > `[`m_vtFluencyGroup`](#class_scorer_1abf7efd49b4940badb9ec90df5c3653a7) | 
`protected bool `[`hasEnding`](#class_scorer_1adc02b2b83020e3b65d2d32c55d6e2afe)`(std::string const & fullString,std::string const & ending)` | 
`protected void `[`DoGrouping`](#class_scorer_1a762cd0ee22194552980857a60f6db4ca)`(std::string & text,std::string & separator,std::vector< std::string > & result)` | 
`protected inline `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` & `[`GetNextPhoneItem`](#class_scorer_1a63159e0bdd62157b709f15575919f0f9)`()` | 
`protected inline size_t `[`GetCurrentPhoneIndex`](#class_scorer_1a151b9047595c5f5219e76af5a2bf903b)`()` | 

## Members

#### `public inline  `[`Scorer`](#class_scorer_1a78a058b089bea56c1f1f97fa1981806b)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` 

#### `public inline virtual  `[`~Scorer`](#class_scorer_1a327de016aeef0e88858c6a99acb4da28)`()` 

#### `public void `[`SetPhoneItem`](#class_scorer_1a14423461af8429095721a7f1ede040e6)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phone_items)` 

#### `public void `[`SetPhoneRefItem`](#class_scorer_1ab607b509878f65be3ac2967a46d5e720)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_ref_items)` 

#### `public void `[`SetWordItem`](#class_scorer_1a34adbb8d192a3fb7f60619987a5ce8dc)`(std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > & word_items)` 

#### `public void `[`DoPhoneScoring`](#class_scorer_1aaa69d47fd2799d9b79d13b04b11ddfd3)`()` 

#### `public void `[`DoWordScoring`](#class_scorer_1ae1b65cdf255080b24bb638d08a75539b)`()` 

#### `public void `[`DoSyllabification`](#class_scorer_1a32574dce8fe3d75c2c3a7084be9395ed)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` 

#### `public void `[`DoFluency_v2`](#class_scorer_1a28567753ed960618eafaad21e5329ed6)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` 

#### `public std::string `[`GetResult`](#class_scorer_1a32c9ac75e8a8b45d11cc0a9dac22f83b)`(std::vector< std::vector< std::string > > & vt_word_sentence)` 

#### `protected `[`ASRContext`](#struct_a_s_r_context)` * `[`m_pASRContext`](#class_scorer_1a735cfb3798b1f6c4f385cdd49089faec) 

#### `protected ScoreSettings * `[`m_pScoreSettings`](#class_scorer_1a9f75f61238f7e360aa733da6067228a9) 

#### `protected std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > `[`phone_items_`](#class_scorer_1afad57f1dd4807e9c5417b03c4f9087b3) 

#### `protected std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > `[`phone_ref_items_`](#class_scorer_1af00cc35a3e2ea75ce25424f89913d18d) 

#### `protected std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > `[`word_items_`](#class_scorer_1a57b6d100cddaff98e5cd7c13b68b841c) 

#### `protected std::vector< `[`stSENTENCE_ITEM`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m)` > `[`sentence_items_`](#class_scorer_1a4e7aaa2a3f49ced1ef79d1d442f9ece0) 

#### `protected std::stringstream `[`result_stream_`](#class_scorer_1a10cb999d477b7508dfa507348d0e1cee) 

#### `protected size_t `[`phone_index_`](#class_scorer_1a56689342445ad7d6327a4990c809c8c4) 

#### `protected rapidjson::Document `[`document_`](#class_scorer_1ab738343606b987a6073982f0bbe00d9d) 

#### `protected size_t `[`sil_phone_count_`](#class_scorer_1a39d8e0ccd909cefc32ee3a3bbc7f3834) 

#### `protected size_t `[`sil_between_sentences_count_`](#class_scorer_1a1f7102e65168ef8d25c9b46745dd5671) 

#### `protected size_t `[`sil_between_words_count_`](#class_scorer_1aea7d59c796301f691a0fdc6092b62edc) 

#### `protected double `[`sil_between_sentence_score_`](#class_scorer_1aa8873740ee04da08e0cad7bc3198381a) 

#### `protected std::vector< double > `[`sil_within_sentence_score_`](#class_scorer_1aa1c67b7c50577658240a987e3816d932) 

#### `protected std::vector< std::string > `[`m_vtConsonants`](#class_scorer_1a1a8b024c50241cba1d887f6717046ac7) 

#### `protected std::vector< std::string > `[`m_vtVowels`](#class_scorer_1a949a9e4eedd29939df7ed5610dae8a1c) 

#### `protected std::vector< std::string > `[`m_vtOnsets`](#class_scorer_1a857150f08a4ce2a500fbdd239d8026b2) 

#### `protected std::vector< std::string > `[`m_vtPauses`](#class_scorer_1a617d0c3fd99aa1c73aa6b8782be6196c) 

#### `protected std::vector< `[`stFLUENCY_GROUP`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p)` > `[`m_vtFluencyGroup`](#class_scorer_1abf7efd49b4940badb9ec90df5c3653a7) 

#### `protected bool `[`hasEnding`](#class_scorer_1adc02b2b83020e3b65d2d32c55d6e2afe)`(std::string const & fullString,std::string const & ending)` 

#### `protected void `[`DoGrouping`](#class_scorer_1a762cd0ee22194552980857a60f6db4ca)`(std::string & text,std::string & separator,std::vector< std::string > & result)` 

#### `protected inline `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` & `[`GetNextPhoneItem`](#class_scorer_1a63159e0bdd62157b709f15575919f0f9)`()` 

#### `protected inline size_t `[`GetCurrentPhoneIndex`](#class_scorer_1a151b9047595c5f5219e76af5a2bf903b)`()` 

# class `ScorerKR` 

```
class ScorerKR
  : public Scorer
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline  `[`ScorerKR`](#class_scorer_k_r_1a63dbfe3091d1f2287a9be0b47226c8ed)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` | 
`public virtual void `[`DoPhoneScoring`](#class_scorer_k_r_1a93d699c423ed503c46d16902da87f3d2)`()` | 
`public virtual void `[`DoWordScoring`](#class_scorer_k_r_1a4102bcb5f2cf38b86d50db693a5fca4c)`()` | 
`public virtual void `[`DoSyllabification`](#class_scorer_k_r_1a5d9f8f821d34c3bdff1384bcaec5fa7c)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` | 
`public virtual void `[`DoFluency_v2`](#class_scorer_k_r_1a45ec3e61597252bd34f513e6c7c2e1bf)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` | 
`public virtual std::string `[`GetResult`](#class_scorer_k_r_1abee253383c8623cddba16600c7d19a8f)`(std::vector< std::vector< std::string > > & vt_word_sentence)` | 

## Members

#### `public inline  `[`ScorerKR`](#class_scorer_k_r_1a63dbfe3091d1f2287a9be0b47226c8ed)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` 

#### `public virtual void `[`DoPhoneScoring`](#class_scorer_k_r_1a93d699c423ed503c46d16902da87f3d2)`()` 

#### `public virtual void `[`DoWordScoring`](#class_scorer_k_r_1a4102bcb5f2cf38b86d50db693a5fca4c)`()` 

#### `public virtual void `[`DoSyllabification`](#class_scorer_k_r_1a5d9f8f821d34c3bdff1384bcaec5fa7c)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` 

#### `public virtual void `[`DoFluency_v2`](#class_scorer_k_r_1a45ec3e61597252bd34f513e6c7c2e1bf)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` 

#### `public virtual std::string `[`GetResult`](#class_scorer_k_r_1abee253383c8623cddba16600c7d19a8f)`(std::vector< std::vector< std::string > > & vt_word_sentence)` 

# class `ScorerUK` 

```
class ScorerUK
  : public Scorer
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`ScorerUK`](#class_scorer_u_k_1a3a2b923062c132f0fd2e4a1cd52e1546)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` | 
`public virtual void `[`DoPhoneScoring`](#class_scorer_u_k_1a997f686b78e29330576ddf59237688b3)`()` | 
`public virtual void `[`DoWordScoring`](#class_scorer_u_k_1af9acccc59fdbd99a66b9ac437a794534)`()` | 
`public virtual void `[`DoSyllabification`](#class_scorer_u_k_1ada97e88195334371c32bbc05d7fb30b9)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` | 
`public virtual void `[`DoFluency_v2`](#class_scorer_u_k_1a322ea64896b9e5a36638a199c6b86259)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` | 
`public virtual std::string `[`GetResult`](#class_scorer_u_k_1a06228df899329fc63288a9ff80d4e263)`(std::vector< std::vector< std::string > > & vt_word_sentence)` | 

## Members

#### `public  `[`ScorerUK`](#class_scorer_u_k_1a3a2b923062c132f0fd2e4a1cd52e1546)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` 

#### `public virtual void `[`DoPhoneScoring`](#class_scorer_u_k_1a997f686b78e29330576ddf59237688b3)`()` 

#### `public virtual void `[`DoWordScoring`](#class_scorer_u_k_1af9acccc59fdbd99a66b9ac437a794534)`()` 

#### `public virtual void `[`DoSyllabification`](#class_scorer_u_k_1ada97e88195334371c32bbc05d7fb30b9)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` 

#### `public virtual void `[`DoFluency_v2`](#class_scorer_u_k_1a322ea64896b9e5a36638a199c6b86259)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` 

#### `public virtual std::string `[`GetResult`](#class_scorer_u_k_1a06228df899329fc63288a9ff80d4e263)`(std::vector< std::vector< std::string > > & vt_word_sentence)` 

# class `ScorerUS` 

```
class ScorerUS
  : public Scorer
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`ScorerUS`](#class_scorer_u_s_1a3c29f061cc2717ff348ff279f7f46d16)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` | 
`public virtual void `[`DoPhoneScoring`](#class_scorer_u_s_1a96757c5bd0b0f4f8aa52a7b283b4d300)`()` | 
`public virtual void `[`DoWordScoring`](#class_scorer_u_s_1a585c95b33095a40d829752614e4dfe0a)`()` | 
`public virtual void `[`DoSyllabification`](#class_scorer_u_s_1a92d2c954c6f92f3cc758b2921e453f22)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` | 
`public virtual void `[`DoFluency_v2`](#class_scorer_u_s_1a90af6d5813bb571f30bfea04c75b7194)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` | 
`public virtual std::string `[`GetResult`](#class_scorer_u_s_1ac6108ae7dd3df78437d096bf932d02c8)`(std::vector< std::vector< std::string > > & vt_word_sentence)` | 

## Members

#### `public  `[`ScorerUS`](#class_scorer_u_s_1a3c29f061cc2717ff348ff279f7f46d16)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` 

#### `public virtual void `[`DoPhoneScoring`](#class_scorer_u_s_1a96757c5bd0b0f4f8aa52a7b283b4d300)`()` 

#### `public virtual void `[`DoWordScoring`](#class_scorer_u_s_1a585c95b33095a40d829752614e4dfe0a)`()` 

#### `public virtual void `[`DoSyllabification`](#class_scorer_u_s_1a92d2c954c6f92f3cc758b2921e453f22)`(std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` 

#### `public virtual void `[`DoFluency_v2`](#class_scorer_u_s_1a90af6d5813bb571f30bfea04c75b7194)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref)` 

#### `public virtual std::string `[`GetResult`](#class_scorer_u_s_1ac6108ae7dd3df78437d096bf932d02c8)`(std::vector< std::vector< std::string > > & vt_word_sentence)` 

# class `Scoring` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`Scoring`](#class_scoring_1a1b25547549812e846ca6d2a9ed92b45f)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` | 
`public virtual  `[`~Scoring`](#class_scoring_1a84e7a2c96b0cabb0bcb8587aca736803)`()` | 
`public void `[`SetPhoneItem`](#class_scoring_1af99098d1d9b410d2a56317a048d724ac)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_items)` | 
`public void `[`SetPhoneRefItem`](#class_scoring_1a505a5b65c6dacd59cf7c8282d422e692)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_ref_items)` | 
`public void `[`SetWordItem`](#class_scoring_1a32a39d39a5f44103c2a5419b21d9f068)`(std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > & words_items)` | 
`public void `[`DoScoring`](#class_scoring_1ab3a26fc534d889f534f96cf453d28fb2)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref,std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` | 
`public std::string `[`GetResult`](#class_scoring_1a5186480cdb0ed32d3db9512dc7c51b23)`(std::string & ref_text,std::vector< std::vector< std::string > > & vt_word_sentence)` | 

## Members

#### `public  `[`Scoring`](#class_scoring_1a1b25547549812e846ca6d2a9ed92b45f)`(`[`ASRContext`](#struct_a_s_r_context)` * pASRContext,ScoreSettings * pScoreSettings)` 

#### `public virtual  `[`~Scoring`](#class_scoring_1a84e7a2c96b0cabb0bcb8587aca736803)`()` 

#### `public void `[`SetPhoneItem`](#class_scoring_1af99098d1d9b410d2a56317a048d724ac)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_items)` 

#### `public void `[`SetPhoneRefItem`](#class_scoring_1a505a5b65c6dacd59cf7c8282d422e692)`(std::vector< `[`stPHONE_ITEM`](#struct____st_p_h_o_n_e___i_t_e_m)` > & phones_ref_items)` 

#### `public void `[`SetWordItem`](#class_scoring_1a32a39d39a5f44103c2a5419b21d9f068)`(std::vector< `[`stWORD_ITEM`](#struct____st_w_o_r_d___i_t_e_m)` > & words_items)` 

#### `public void `[`DoScoring`](#class_scoring_1ab3a26fc534d889f534f96cf453d28fb2)`(stFEATURE_RESULT & feats,stFEATURE_RESULT & feats_ref,std::vector< std::string > & syll_phn,std::vector< std::string > & syll_ltr)` 

#### `public std::string `[`GetResult`](#class_scoring_1a5186480cdb0ed32d3db9512dc7c51b23)`(std::string & ref_text,std::vector< std::vector< std::string > > & vt_word_sentence)` 

# struct `__stFLUENCY_GROUP` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public std::vector< double > `[`vtScores`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a4b8053ab51010e22d7c12512218ac362) | 
`public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtPitchLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1ad44449c001b6a8c5d34d0be67fa209a2) | 
`public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtIntensityLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a5379f026ed855e9f841ece4cde089e97) | 
`public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtDurationLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a2756896a5790ce6004048d76d692b301) | 

## Members

#### `public std::vector< double > `[`vtScores`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a4b8053ab51010e22d7c12512218ac362) 

#### `public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtPitchLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1ad44449c001b6a8c5d34d0be67fa209a2) 

#### `public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtIntensityLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a5379f026ed855e9f841ece4cde089e97) 

#### `public std::vector< `[`stLABEL`](#struct____st_l_a_b_e_l)` > `[`vtDurationLabel`](#struct____st_f_l_u_e_n_c_y___g_r_o_u_p_1a2756896a5790ce6004048d76d692b301) 

# struct `__stLABEL` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public std::string `[`unit`](#struct____st_l_a_b_e_l_1af64b5b3b9542624e293664e473787c3b) | 
`public double `[`ref_value`](#struct____st_l_a_b_e_l_1abec629d90c06ed006c13e7eb2cd028a1) | 
`public double `[`value`](#struct____st_l_a_b_e_l_1afba697fe6cfda60344737732b58ef056) | 

## Members

#### `public std::string `[`unit`](#struct____st_l_a_b_e_l_1af64b5b3b9542624e293664e473787c3b) 

#### `public double `[`ref_value`](#struct____st_l_a_b_e_l_1abec629d90c06ed006c13e7eb2cd028a1) 

#### `public double `[`value`](#struct____st_l_a_b_e_l_1afba697fe6cfda60344737732b58ef056) 

# struct `__stPHONE_ITEM` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public int32_t `[`id`](#struct____st_p_h_o_n_e___i_t_e_m_1a3aa915076028e4f81f23b6c62b1ef23c) | 
`public std::string `[`phone`](#struct____st_p_h_o_n_e___i_t_e_m_1aa73d4c096a6e76d75b593796b6c97e94) | 
`public std::string `[`phone_base`](#struct____st_p_h_o_n_e___i_t_e_m_1a0d45c5703a412a16e7575f3b131e5924) | 
`public std::string `[`phone_accent`](#struct____st_p_h_o_n_e___i_t_e_m_1a5752504a87308cfa20e99dcb05c5c118) | 
`public double `[`time_start`](#struct____st_p_h_o_n_e___i_t_e_m_1aabb4e7d7dab6ad123c3759ca713e64e4) | 
`public double `[`time_duration`](#struct____st_p_h_o_n_e___i_t_e_m_1aff916efd0c259510646c300d0ba3b88b) | 
`public int32_t `[`repeat_count`](#struct____st_p_h_o_n_e___i_t_e_m_1a1332dd16366e7439832b7de6e994221a) | 
`public double `[`loglikelihood`](#struct____st_p_h_o_n_e___i_t_e_m_1a86f9091c78b6e2910d080c6e4680b991) | 
`public double `[`score`](#struct____st_p_h_o_n_e___i_t_e_m_1ad98b471c5eae4240b126b824e8611874) | 
`public double `[`pitch`](#struct____st_p_h_o_n_e___i_t_e_m_1a808d75e40965331d5dd7505f95d2fdff) | 
`public double `[`intensity`](#struct____st_p_h_o_n_e___i_t_e_m_1a545e79ee4f4a24fd7eb7b31cf6d18d72) | 

## Members

#### `public int32_t `[`id`](#struct____st_p_h_o_n_e___i_t_e_m_1a3aa915076028e4f81f23b6c62b1ef23c) 

#### `public std::string `[`phone`](#struct____st_p_h_o_n_e___i_t_e_m_1aa73d4c096a6e76d75b593796b6c97e94) 

#### `public std::string `[`phone_base`](#struct____st_p_h_o_n_e___i_t_e_m_1a0d45c5703a412a16e7575f3b131e5924) 

#### `public std::string `[`phone_accent`](#struct____st_p_h_o_n_e___i_t_e_m_1a5752504a87308cfa20e99dcb05c5c118) 

#### `public double `[`time_start`](#struct____st_p_h_o_n_e___i_t_e_m_1aabb4e7d7dab6ad123c3759ca713e64e4) 

#### `public double `[`time_duration`](#struct____st_p_h_o_n_e___i_t_e_m_1aff916efd0c259510646c300d0ba3b88b) 

#### `public int32_t `[`repeat_count`](#struct____st_p_h_o_n_e___i_t_e_m_1a1332dd16366e7439832b7de6e994221a) 

#### `public double `[`loglikelihood`](#struct____st_p_h_o_n_e___i_t_e_m_1a86f9091c78b6e2910d080c6e4680b991) 

#### `public double `[`score`](#struct____st_p_h_o_n_e___i_t_e_m_1ad98b471c5eae4240b126b824e8611874) 

#### `public double `[`pitch`](#struct____st_p_h_o_n_e___i_t_e_m_1a808d75e40965331d5dd7505f95d2fdff) 

#### `public double `[`intensity`](#struct____st_p_h_o_n_e___i_t_e_m_1a545e79ee4f4a24fd7eb7b31cf6d18d72) 

# struct `__stSENTENCE_ITEM` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public int32_t `[`id`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a476fa90d75e197a68e9d27f528ebbceb) | 
`public std::string `[`text`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a83466a913a4f5bdf110a1aae4e36d431) | 
`public int32_t `[`word_item_start_index`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a7c6d87ce312ebafc2b44362f64de88bd) | 
`public int32_t `[`word_item_end_index`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a8effa19d21791923f69402256da9ba1f) | 
`public int32_t `[`repeat_count`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a0edd1a006746f0b97b3d8711d9071151) | 
`public double `[`score`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1ae141b2edd91bf742f25726bfb597d95a) | 
`public double `[`start`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1af97c72174e14331feb4f897889833370) | 
`public double `[`end`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1af12711fa1a2b247637aa83e7d861f6c3) | 

## Members

#### `public int32_t `[`id`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a476fa90d75e197a68e9d27f528ebbceb) 

#### `public std::string `[`text`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a83466a913a4f5bdf110a1aae4e36d431) 

#### `public int32_t `[`word_item_start_index`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a7c6d87ce312ebafc2b44362f64de88bd) 

#### `public int32_t `[`word_item_end_index`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a8effa19d21791923f69402256da9ba1f) 

#### `public int32_t `[`repeat_count`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1a0edd1a006746f0b97b3d8711d9071151) 

#### `public double `[`score`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1ae141b2edd91bf742f25726bfb597d95a) 

#### `public double `[`start`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1af97c72174e14331feb4f897889833370) 

#### `public double `[`end`](#struct____st_s_e_n_t_e_n_c_e___i_t_e_m_1af12711fa1a2b247637aa83e7d861f6c3) 

# struct `__stSYLL_LETTER_ITEM` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public std::string `[`text`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m_1a438c377fcb9bf0fb0fc932a8e3b287b6) | 
`public double `[`score`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m_1a04c5466802f1f3077ec2d535bce2e969) | 

## Members

#### `public std::string `[`text`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m_1a438c377fcb9bf0fb0fc932a8e3b287b6) 

#### `public double `[`score`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m_1a04c5466802f1f3077ec2d535bce2e969) 

# struct `__stSYLL_PHONE_ITEM` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public int32_t `[`index`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ae6f58fc18dc1647936e8626f24f6f8b6) | 
`public std::string `[`text`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1a3bae0a9996c32d1f3f52272e731df8c3) | 
`public double `[`score`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ab55c9e8bd79af86c20db3f5c8d7e6f4b) | 
`public double `[`duration`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1a7eab629283eb2a86046bb6679ef25879) | 
`public int16_t `[`stress`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ae73564be9c1497b05a53694bb66e3f09) | 

## Members

#### `public int32_t `[`index`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ae6f58fc18dc1647936e8626f24f6f8b6) 

#### `public std::string `[`text`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1a3bae0a9996c32d1f3f52272e731df8c3) 

#### `public double `[`score`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ab55c9e8bd79af86c20db3f5c8d7e6f4b) 

#### `public double `[`duration`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1a7eab629283eb2a86046bb6679ef25879) 

#### `public int16_t `[`stress`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m_1ae73564be9c1497b05a53694bb66e3f09) 

# struct `__stWORD_ITEM` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public int32_t `[`id`](#struct____st_w_o_r_d___i_t_e_m_1a60dab1a777081681791512b500bfc53c) | 
`public std::string `[`word`](#struct____st_w_o_r_d___i_t_e_m_1a8fb1da1d2d1a17f94d68e92847283a66) | 
`public int32_t `[`phone_item_start_index`](#struct____st_w_o_r_d___i_t_e_m_1a4c07826945c64eb33b28de970ce33df6) | 
`public int32_t `[`phone_item_end_index`](#struct____st_w_o_r_d___i_t_e_m_1ae8e0e0ac81e05e5b0def322ea6f01c4a) | 
`public double `[`time_start`](#struct____st_w_o_r_d___i_t_e_m_1a515521b629ff31bfe6c0c4c94bee97f0) | 
`public double `[`time_duration`](#struct____st_w_o_r_d___i_t_e_m_1aa723b9c70c2366cb130bea26c2abbe43) | 
`public int32_t `[`repeat_count`](#struct____st_w_o_r_d___i_t_e_m_1a0c62689ec9021afd3320329f1d9685d6) | 
`public double `[`score`](#struct____st_w_o_r_d___i_t_e_m_1af654ea054320d24beceba1341f08e003) | 
`public std::vector< std::vector< `[`stSYLL_PHONE_ITEM`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m)` > > `[`syll_phn`](#struct____st_w_o_r_d___i_t_e_m_1a0e38a2cbc3d015e1b33a84e7fedaf097) | 
`public std::vector< std::vector< `[`stSYLL_LETTER_ITEM`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m)` > > `[`syll_ltr`](#struct____st_w_o_r_d___i_t_e_m_1a753da7c841a3fc021f28bb4a559cd873) | 

## Members

#### `public int32_t `[`id`](#struct____st_w_o_r_d___i_t_e_m_1a60dab1a777081681791512b500bfc53c) 

#### `public std::string `[`word`](#struct____st_w_o_r_d___i_t_e_m_1a8fb1da1d2d1a17f94d68e92847283a66) 

#### `public int32_t `[`phone_item_start_index`](#struct____st_w_o_r_d___i_t_e_m_1a4c07826945c64eb33b28de970ce33df6) 

#### `public int32_t `[`phone_item_end_index`](#struct____st_w_o_r_d___i_t_e_m_1ae8e0e0ac81e05e5b0def322ea6f01c4a) 

#### `public double `[`time_start`](#struct____st_w_o_r_d___i_t_e_m_1a515521b629ff31bfe6c0c4c94bee97f0) 

#### `public double `[`time_duration`](#struct____st_w_o_r_d___i_t_e_m_1aa723b9c70c2366cb130bea26c2abbe43) 

#### `public int32_t `[`repeat_count`](#struct____st_w_o_r_d___i_t_e_m_1a0c62689ec9021afd3320329f1d9685d6) 

#### `public double `[`score`](#struct____st_w_o_r_d___i_t_e_m_1af654ea054320d24beceba1341f08e003) 

#### `public std::vector< std::vector< `[`stSYLL_PHONE_ITEM`](#struct____st_s_y_l_l___p_h_o_n_e___i_t_e_m)` > > `[`syll_phn`](#struct____st_w_o_r_d___i_t_e_m_1a0e38a2cbc3d015e1b33a84e7fedaf097) 

#### `public std::vector< std::vector< `[`stSYLL_LETTER_ITEM`](#struct____st_s_y_l_l___l_e_t_t_e_r___i_t_e_m)` > > `[`syll_ltr`](#struct____st_w_o_r_d___i_t_e_m_1a753da7c841a3fc021f28bb4a559cd873) 

# struct `ASRContext` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public FeatureSettings `[`Feature`](#struct_a_s_r_context_1a212bc734e57ea83e18ee0aeb50057b0e) | 
`public DecodeSettings `[`Decode`](#struct_a_s_r_context_1ad8d0924207a09dc7f0549ba0efdda841) | 
`public EndpointSettings `[`Endpoint`](#struct_a_s_r_context_1a69626eaea8f64afd0b4c25cfd5072a01) | 
`public ModelSettings `[`Model`](#struct_a_s_r_context_1a6f55e313099c0a439a38fc636422ddf6) | 
`public ScoreSettings `[`Score`](#struct_a_s_r_context_1ae2169dd09756393c765e21541f351f31) | 
`public kaldi::TransitionModel `[`m_TransitionModel`](#struct_a_s_r_context_1a11c33e72b1fa0ee202d04e3c66c6e059) | 
`public kaldi::nnet2::AmNnet `[`m_AmNnet`](#struct_a_s_r_context_1a981fbf0fc6609afda5fe5986d6231fdf) | 
`public fst::Fst< fst::StdArc > * `[`m_pDecodeFst`](#struct_a_s_r_context_1a398624dee3d305c6114376f8116fcb12) | 
`public fst::SymbolTable * `[`m_pWordSym`](#struct_a_s_r_context_1a079bc55d0b748e96506b2b23ef25f9f0) | 
`public fst::SymbolTable * `[`m_pPhoneSym`](#struct_a_s_r_context_1a31ac2cbcc3caa19251682297b9ce328d) | 
`public std::string `[`m_strErrorMessage`](#struct_a_s_r_context_1a2515feef990abaae02c41b67ee3532e3) | 
`public std::mutex `[`m_mtxSession`](#struct_a_s_r_context_1a07efa76e8d090d56835e3a9d3fa7854d) | 
`public  `[`ASRContext`](#struct_a_s_r_context_1a5bd5abc2ddbade56f2472c15d6a2ecc0)`()` | 
`public  `[`~ASRContext`](#struct_a_s_r_context_1abcce3aada9d83a2ba8b1e5412b6a36d4)`()` | 
`public bool `[`Load`](#struct_a_s_r_context_1ad0a89ea18ebca8d68c1154b8e6b2ef33)`()` | 
`public `[`ASRSession`](#struct_a_s_r_session)` * `[`CreateSession`](#struct_a_s_r_context_1a96d340d5368c321970717245537a0824)`()` | 

## Members

#### `public FeatureSettings `[`Feature`](#struct_a_s_r_context_1a212bc734e57ea83e18ee0aeb50057b0e) 

#### `public DecodeSettings `[`Decode`](#struct_a_s_r_context_1ad8d0924207a09dc7f0549ba0efdda841) 

#### `public EndpointSettings `[`Endpoint`](#struct_a_s_r_context_1a69626eaea8f64afd0b4c25cfd5072a01) 

#### `public ModelSettings `[`Model`](#struct_a_s_r_context_1a6f55e313099c0a439a38fc636422ddf6) 

#### `public ScoreSettings `[`Score`](#struct_a_s_r_context_1ae2169dd09756393c765e21541f351f31) 

#### `public kaldi::TransitionModel `[`m_TransitionModel`](#struct_a_s_r_context_1a11c33e72b1fa0ee202d04e3c66c6e059) 

#### `public kaldi::nnet2::AmNnet `[`m_AmNnet`](#struct_a_s_r_context_1a981fbf0fc6609afda5fe5986d6231fdf) 

#### `public fst::Fst< fst::StdArc > * `[`m_pDecodeFst`](#struct_a_s_r_context_1a398624dee3d305c6114376f8116fcb12) 

#### `public fst::SymbolTable * `[`m_pWordSym`](#struct_a_s_r_context_1a079bc55d0b748e96506b2b23ef25f9f0) 

#### `public fst::SymbolTable * `[`m_pPhoneSym`](#struct_a_s_r_context_1a31ac2cbcc3caa19251682297b9ce328d) 

#### `public std::string `[`m_strErrorMessage`](#struct_a_s_r_context_1a2515feef990abaae02c41b67ee3532e3) 

#### `public std::mutex `[`m_mtxSession`](#struct_a_s_r_context_1a07efa76e8d090d56835e3a9d3fa7854d) 

#### `public  `[`ASRContext`](#struct_a_s_r_context_1a5bd5abc2ddbade56f2472c15d6a2ecc0)`()` 

#### `public  `[`~ASRContext`](#struct_a_s_r_context_1abcce3aada9d83a2ba8b1e5412b6a36d4)`()` 

#### `public bool `[`Load`](#struct_a_s_r_context_1ad0a89ea18ebca8d68c1154b8e6b2ef33)`()` 

#### `public `[`ASRSession`](#struct_a_s_r_session)` * `[`CreateSession`](#struct_a_s_r_context_1a96d340d5368c321970717245537a0824)`()` 

# struct `ASRSession` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public kaldi::OnlineIvectorExtractorAdaptationState * `[`pAdaptationState`](#struct_a_s_r_session_1afad8d102e1e529c730e396ac946000c1) | 
`public kaldi::OnlineCmvnState * `[`pCmvnState`](#struct_a_s_r_session_1a57b5a8977e1332efd7da5ae17a376a28) | 
`public kaldi::OnlineNnet2FeaturePipeline * `[`pFeaturePipeline`](#struct_a_s_r_session_1a1dbf1a0a9789b29ec312f865b041ad52) | 
`public inline  `[`~ASRSession`](#struct_a_s_r_session_1a65df242b8920040e5d1871d072c87b26)`()` | 

## Members

#### `public kaldi::OnlineIvectorExtractorAdaptationState * `[`pAdaptationState`](#struct_a_s_r_session_1afad8d102e1e529c730e396ac946000c1) 

#### `public kaldi::OnlineCmvnState * `[`pCmvnState`](#struct_a_s_r_session_1a57b5a8977e1332efd7da5ae17a376a28) 

#### `public kaldi::OnlineNnet2FeaturePipeline * `[`pFeaturePipeline`](#struct_a_s_r_session_1a1dbf1a0a9789b29ec312f865b041ad52) 

#### `public inline  `[`~ASRSession`](#struct_a_s_r_session_1a65df242b8920040e5d1871d072c87b26)`()` 

# struct `ScoringConfig` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public std::string `[`code`](#struct_scoring_config_1affd03dfc937afee9e5b4bf0604805054) | 

## Members

#### `public std::string `[`code`](#struct_scoring_config_1affd03dfc937afee9e5b4bf0604805054) 

Generated by [Moxygen](https://sourcey.com/moxygen)

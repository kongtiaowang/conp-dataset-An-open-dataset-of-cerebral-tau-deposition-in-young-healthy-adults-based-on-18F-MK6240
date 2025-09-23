# An open dataset of cerebral tau deposition in young healthy adults based on [18F]MK6240 positron emission tomography

Crawled from [OSF](https://osf.io/znt9d/)

## Description

Dataset of [18F]MK6240 PET in young healthy adults

## DOI: 10.17605/OSF.IO/ZNT9D

## WIKI

Transformation matrices are included in rawdata/s-0**/ses-01/anat/

To transform PET images in T1w space to MNI152 using ANTs, do the following command:

    antsApplyTransforms
    -i ${derivatives}/sub-${subj}/${ses}/pet/sub-${subj}_${ses}_pvc-none_ref-none_trc-MK6240_pet.nii.gz \
    -r mni_icbm152_t1_tal_nlin_sym_09a.nii.gz \
    -t ${derivatives}/sub-${subj}/${ses}/anat/sub-${subj}_${ses}_from-T1w_to-MNI152_ICBM152_t1_tal_nlin_sym_09a_mode-image_desc-SyN_1Warp.nii.gz \
    -t ${derivatives}/sub-${subj}/${ses}/anat/sub-${subj}_${ses}_from-T1w_to-MNI152_ICBM152_t1_tal_nlin_sym_09a_mode-image_desc-SyN_0GenericAffine.mat \
    -o ${derivatives}/sub-${subj}/${ses}/pet/sub-${subj}_${ses}_space-MNI152_pvc-none_ref-none_trc-MK6240_pet.nii.gz.nii.gz \
    -d 3 -v
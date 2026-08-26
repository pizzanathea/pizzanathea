import { DisplayBlock } from '#/components/atoms/display-block';

import { templates } from '#/resources';
import { CanvasSection } from '#/types';
import { CanvasSection, PanelsEnum } from '#/types';

const MAX_TEMPLATES_DISPLAY = 8;

@@ -41,9 +41,10 @@ export function Welcome() {
.map(({ template }, index) => (
<button
key={index}
                onClick={() =>
                  actions.canvas.preview.sections(template as CanvasSection[])
                }
                onClick={() => {
                  actions.canvas.preview.sections(template as CanvasSection[]);
                  actions.panel.right.show(PanelsEnum.TEMPLATES);
                }}
>
<DisplayBlock.Container>
<DisplayBlock.Content>
